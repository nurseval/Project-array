# Project-array
ıscı-memur-maası-hesaplayan-program

namespace iscimemurmaası


  
{

    internal class Program

    {        
        /*Bir İş yeri için işçi ve memurun haftalık ücret hesabını yapan program hazırlanacaktır. İşçilerin günlük ücreti 100 tl. memurun 120 tl dir.
              * işçi ve memur haftalık 40 aatin üzerinde ki her saat için mesai almaktadır. işçiler saatlil 20 tl, memurlar ise 15 tl mesai almaktadır.
              istenilen çalışan seçilerek maaş hesabı yapacak program tasarlayınız. üçret = çalışma saati x haftalıkgün + mesai(varsa9*/
        
        int isci_ucret(int saat)
        {
            int u, m, ms;
            if(saat > 40)
            {
                ms = saat - 40;
                m = ms * 20;
                u = (100 * 5) + m;
            }
            else
            {
                u = 100 * 5;    
            }
            return u;
        }
        
        int memur_ucret(int saat)
        {
            int u, m, ms;
            if(saat > 40)
            {
                ms = saat - 40;
                m = ms * 15;
                u = (120 * 5) + m;
            }
            else
            {
                u = 120 * 5;
            }
            return u;
        }





        static void Main(string[] args)
        {
            Program cagir = new Program();
            char secici;
            int cs, ucret;
            Console.Write("MAAŞ HESAPLAMA PROGRAMI\n\nI - İşçi Maaşı\nM - Memur Maaşı\nİşlemi Seçiniz.");
            secici = Convert.ToChar(Console.ReadLine());

            switch(secici)
            {
                case 'I':
                    {
                        Console.Write("Haftalık Çalışma Süresi (Saat) :");
                        cs = Convert.ToInt32(Console.ReadLine());
                        ucret = cagir.isci_ucret(cs);
                        Console.WriteLine("İşçinin Maaşı = " + ucret);
                    }break;

                case 'M':
                    {
                        Console.Write("Haftalık Çalışma SÜresi (Saat) :");
                        cs = Convert.ToInt32(Console.ReadLine());
                        ucret = cagir.memur_ucret(cs);
                        Console.WriteLine("Memurun Maaşı = "+ ucret);

                    }break;
                default : Console.WriteLine("Böyle Bir Çalışan Yoktur.");break;
            }

            Console.ReadKey();

        }
    }

}

[Patika Dev Sayfam](https://app.patika.dev/sevaalnuur)





