# using System;

namespace ConsoleApp20
{
    class all
    {
                    
            public string Name { get; set; }

            public virtual void GetName()
            {
                Console.WriteLine("1");
            }

        class Admin : all
        {
            public override void GetName()
            {
                Console.WriteLine("2");
            }
        }



            class Worker : all
            {
                public override void GetName()
                {
                    Console.WriteLine("3");
                }
            }

            class Staff : all
            {
                public override void GetName()
                {
                    Console.WriteLine("4");
                }
            }
            class Engineer : all
            {
                public override void GetName()
                {
                    Console.WriteLine("5");
                }
            }
        class v2
        {
            static void Main()
            {
                all[] All = new all[4];

                Admin admin = new Admin();
                admin.Name = " - admin";

                Worker worker = new Worker();
                worker.Name = " - worker";

                Staff staff = new Staff();
                staff.Name = " - staff";

                Engineer engineer = new Engineer();
                engineer.Name = " - engineer";

                All[0] = admin;
                All[1] = worker;
                All[2] = staff;
                All[3] = engineer;

                for (int i = 0; i < All.Length; i++)
                {
                    All[i].GetName();
                }
                Console.ReadKey();
            }

        }
    }
}
