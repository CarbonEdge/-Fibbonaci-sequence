# -Fibbonaci-sequence
CodeEval - easy
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Fibbonacci
{
    class Program
    {
        static void Main(string[] args)
        {
            try
            {
                using (System.IO.StreamReader reader = new System.IO.StreamReader("C:\\Users\\mchotu\\Documents\\test\\TestFile.txt"))//this should be changed to args[0] when submitted
                {// read text file
                    string line = reader.ReadLine();
                    double c = Math.Sqrt(5);
                    double pi = (1 +c) / 2;
                    while (line != null)
                    {
                        int numVal = Int32.Parse(line);
                        Double Fib = Math.Pow(pi, numVal)/c;
                        Console.WriteLine(Math.Round(Fib));
                        line = reader.ReadLine();//do not delete
                    }//while

                }//using
            }//try
            catch (Exception e)
            {
                Console.WriteLine("The file could not be read:");
                Console.WriteLine(e.Message);
            }
            Console.ReadKey();
        }
    }
}

