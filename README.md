# Konsool3

using System; // video 14

    class Program
    {
        static void Main()
        {
            Console.WriteLine("Please enter your target?"); // Kirjtab esimeseks reaks "Please enter your target?"
        int UserTarget = int.Parse(Console.ReadLine());     // convert a string to an int.

        int Start = 0;                                     // Hakkab lugema numbrid alates  0st 

        while(Start <= UserTarget)                         //Kui number rohkem 0st või võrdub siis edasi on kirjeldatud tingimus
        {
            Console.Write(Start + " ");                    // Hakkab liitma iga numbrile mingi arvu 
            Start = Start + 2;                             // Hakkab liitma 2 iga numbrile 
        }
      }
    }
    

using System;


    class Program
    {
        static void Main(string[] args)    
        {
            string UserChoice = string.Empty;    // muutuv UserChoise, mis pole arv ja string tagastab tühja rida
            do                                   // teeb nii kaua kui while tingimus sobib
            {
                Console.WriteLine("Please enter your target?");
                int UserTarget = int.Parse(Console.ReadLine());

                int Start = 0;

                while (Start <= UserTarget)
                {
                    Console.Write(Start + " ");
                    Start = Start + 2;
                }
                do
                {
                    Console.WriteLine("Do you want to continue - Yes or No?");

                    UserChoice = Console.ReadLine().ToUpper(); // ToUpper pöördub teksti suurteks täheks
                    if (UserChoice != "YES" && UserChoice != "NO")
                    {
                        Console.WriteLine("Invalid Choice, please say Yes or No");
                    }
                } while (UserChoice != "YES" && UserChoice != "NO");
            } while (UserChoice == "YES");
        }
    }
