using FakeItEasy;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

                    // CREATING DISTANCE MATRIX WITH RANDOM COORDINATS 
namespace _2dplane
{
    class Program
    {
        private static readonly Random random = new Random();

        private static double RandomNumberBetween(double minValue, double maxValue)
        {
            var next = random.NextDouble();

            return minValue + Math.Round((next * (maxValue - minValue)),2);
        } // rastgele double değerini istenilen aralıklarda almak için
        static void Main(string[] args)
        {
            PrintCoordinat(10, 100, 100);
            PrintCoordinat(100, 100, 100);
            PrintDistance(10,100,100);
            Console.ReadLine();
        }
         
        static double[,] SizeOfMatrix(int point ,int width, int height )
        {
            double[,] matrix = new double[point, 2];
            for (int i = 0; i < point ; i++)
            {
                for (int j = 0; j < 2; j++)
                {
                    if (j == 0)
                    {
                        double randomnumber = RandomNumberBetween(0, width);
                        matrix[i, j] = randomnumber;
                    }
                    if (j == 1)
                    {
                        double randomnumber = RandomNumberBetween(0, height);
                        matrix[i, j] = randomnumber;
                    }
                }
            }

            return matrix;
        }
        static double[,] DistanceMatrix(int point, int width, int height)
        {
            double[,] distance = new double[point,point];
            double[,] size = new double[point,2];
            size = SizeOfMatrix(point, width, height);
              
            for (int i = 0; i < point; i++)
            {
                int a = 0; // tüm noktalar ile uzaklık hesaplamak için değişken
                    for (int j = 0; j < point; j++)
                {
                    distance[i, j] = Math.Round(Math.Sqrt(Math.Pow(size[i, 0]- size[a,0],2) + Math.Pow(size[i,1]-size[a,1],2)),2);
                    a++;
                }
            }
            return distance;
        }
        static void PrintCoordinat(int point, int width, int height)
        {
            double[,] PrintMatrix = new double[point, 2];
            PrintMatrix = SizeOfMatrix(point, width, height);
            Console.Write("Count of point : ");
            Console.Write("\t"+"X value : ");
            Console.WriteLine("\t"+"Y point : ");
            for (int i = 0; i < point; i++)
            {
                Console.Write((i + 1)+"\t"); //nokta sayılarını göstermek için
                for (int j = 0; j < 2; j++)
                {
                    Console.Write("\t"+ PrintMatrix[i, j]+"\t");
                }
                Console.WriteLine();
            }
            Console.WriteLine();
        }
        static void PrintDistance(int point, int width, int height)
        {
            double[,] distance1 = new double[point, point];
            distance1 = DistanceMatrix(point, width, height);
            Console.WriteLine("Distance Matrix is : ");
            Console.WriteLine();
            for (int i = 0; i < point; i++)
            {
                for (int j = 0; j < point; j++)
                {
                    Console.Write(distance1[i, j]+"\t");

                }
                Console.WriteLine();
            }
        }
       
    }

}
