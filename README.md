# CF-1461A_String-generation
using System;

namespace string_generation
{
    class Program
    {
        static void Main(string[] args)
        {
            int t = Convert.ToInt32(Console.ReadLine());
            while(t>0)
            {
                t--;
                int flag = 0, n, k;
                var text = (Console.ReadLine()).Split(' ');
                n = int.Parse(text[0]);
                k = int.Parse(text[1]);
                string str = "";
                for (int i = 0; i < k; i++)
                    str += 'a';
                for (int i = k; i < n; i++)
                {
                    if (flag == 0)
                    {
                        str += 'b';
                        flag = 1;
                    }
                    else
                        if (flag == 1)
                    {
                        str += 'c';
                        flag = 2;
                    }
                    else
                    {
                        str += 'a';
                        flag = 0;
                    }
                }
                Console.WriteLine(str);
            }
        }
    }
}
