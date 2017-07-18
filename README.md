# DNA-Sequences
Just another repository
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace DNA_Sequences
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            int a = 0;
            int c = 0;
            int g = 0;
            int t = 0;
            int sum = 0;

            for (char i = 'A'; i <= 'T'; i++)
            {
                if (i == 'A' || i == 'C' || i == 'G' || i == 'T')
                {

                    sum++;
                    for (char j = 'A'; j <= 'T'; j++)
                    {
                        if (j == 'A' || j == 'C' || j == 'G' || j == 'T')
                        {
                            sum++;
                            for (char k = 'A'; k <= 'T'; k++)
                            {
                                if (k == 'A' || k == 'C' || k == 'G' || k == 'T')
                                {
                                    sum++;
                                    if (k == 'T')
                                    {
                                        if (sum >= n)
                                        {
                                            Console.WriteLine("O{0}{1}{2}O ", i, j, k);
                                        }
                                        else
                                        {
                                            Console.WriteLine("X{0}{1}{2}X ", i, j, k);
                                        }
                                    }
                                    else
                                    {
                                    if (sum >= n)
                                    {
                                        Console.Write("O{0}{1}{2}O ", i, j, k);
                                    }
                                    else
                                    {
                                        Console.Write("X{0}{1}{2}X ", i, j, k);
                                    }
                                    }
                                }
                                if (k == 'T')
                                {
                                    sum -= 4;
                                }
                            }
                        }
                        if (j == 'T')
                        {
                            sum -= 4;
                        }
                    }
                }
                
            }
        }
    }
}
