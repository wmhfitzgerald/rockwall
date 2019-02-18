using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
namespace Rockwall {
    class Program {
        public static void Main() {
           //drawRockWall(9,5);
           drawRockWall(20, 12);
        }        
        private static void drawRockWall(int w, int h) {
            string x = "x";
            int b = 0;
            int c = 1;            
            int k = 0;
            int l = 1;            
            for (int i=0; i < h; i++){                
                Console.Write("|");                 
                if(i%2 == 0){                    
                    for (int y=1; y <= b; y++){
                        Console.Write(" ");
                    }                    
                    for (int z=0; z <= b; z++){                
                        Console.Write("x");
                    }           
                    for (int o=c; o < w; o++){
                        Console.Write(" ");
                    }                  
                  b++;
                  c+=2;                  
                }else{                    
                    for (int o=l; o < w; o++){
                        Console.Write(" ");
                    }                    
                    for (int z=0; z <= k; z++){                
                        Console.Write("x");
                    }                    
                    for (int y=1; y <= k; y++){
                        Console.Write(" ");
                    }                    
                  k++;
                  l+=2;
                }               
                Console.WriteLine("|"); 
            }   
        }
    }
}
