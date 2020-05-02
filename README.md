# NAVICATORMEX
# repo-Mexico
# project:NAVICATORMEX
# México
# COVID-MEX19
using System;  
using System.Configuration;  
  
namespace ConsoleApplication 
{  
    class Program	//Declaring an object of type MyClass.
MyClass mc = new MyClass();
192.168.1.1 

* $git chekout - b A780L3C

Siwtched to a new branch "A780L3C"

* $ git branch
 	
* El '''[[MS-Dos|Símbolo del Sistema]]''', BIOS ''STUP UTILITY'' y precede al ''(A78LK-M3S)''
* El '''[[USB-2.0|Module Versión - 2.24.3-13.4]]'''
 		 	
 	
== v2.0 (C) Copyright Años '''1985-2006''',American Megatrends, inc ==

* De él año '''[[1985]]'''
* A él año '''[[2006]]'''

== Wimdows Vista, Wimdows Update, Wimdows 7-8, Power Shell, Wimdows 10 ==
 	
== OnDriver ==

* $Disco local
* $Documentos
* $C:/Wimdows/usuarios/navicatormexsinchayote@gmail.com/system32/cmd.exe

== Google Drive ==

* Dowload
* Enmulated
* Android
* Huawei
* Tarjeta Sd Card

== microsoft.com.mx ==

* [[Cuenta de microsoft.com.mx|"navicatormexsinchayote@gmail.com"]]
* [[Cuenta de trabajo microsoft.com.mx|"navicatormex@huertaas.onmicrosoft.com"]]

=== System Overview ===

* '''[[AMIBIOS]]'''
* Version	:08.00.14
* Build Date	:07/31/12
* '''System Memory'''
* Size	:4096

* System Time	[12:23:..]
* System Date	[Sab 04/02/2020]

 	
=== Sistemas Operativos ===

* '''[[DOS]]''', para computadora personal. HUAWEI Pro Y6 2018 versión 8.0
* '''[[DR-DOS]]''', de Digital Research.
* '''[[DR-DOS]]''', de Digital Investigación, Microsoft, Visual Estudio
* '''[[Freedom House|FreeDOS]]'''. <code>'''Sistem Overview,'''</code> '''AMIBIOS''' ''Versión	:08.00.14'', ''Build Date	:07/31/12''
* '''[[MS-DOS]]''', de Microsoft.
* '''[[PC-DOS]]''', de IBM.
* '''[[QDOS]]''', escrito por Tim Paterson.
* '''[[android DOS]]''', de web.
 	
* '''[[Main PC: "AMIBIOS" Vesion	08.00.14 MS-DOS]]''', de v2.61 (C)Copyright 1985-2006,American Megatrends, Inc.
 		 	
* '''[[Android DOS (Hidalgo, México)|MS-DOS]]''',) '''[[MS-DOS (Código Postal:42700")|Android DOS]]''' Mixquiahuala de Juárez, Hidalgo. México
* '''MS-DOS,''' México, City México, City/MEX. [https://microsoft.com.mx,+Microsoft,+Estados+Unidos Microsoft, México, Microsoft, Inc]


//Declaring another object of the same type, assigning it the value of the first object.
MyClass mc2 = mc;
    {  
        static void Main(string[] args)  
        {  
            ReadAllSettings();  
            ReadSetting("Setting1");  
            ReadSetting("NotValid");  
            AddUpdateAppSettings("NewSetting", "Mar 01, 2020");  
            AddUpdateAppSettings("Setting1", "Mar 01, 2022");  
            ReadAllSettings();  
        }  
  
        static void ReadAllSettings()  
        {  
            try  
            {  
                var appSettings = ConfigurationManager.AppSettings;  
  
                if (appSettings.Count == 0)  
                {  
                    Console.WriteLine("AppSettings is empty.");  
                }  
                else  
                {  
                    foreach (var key in appSettings.AllKeys)  
                    {  
                        Console.WriteLine("Key: {0} Value: {1}", key, appSettings[key]);  
                    }  
                }  
            }  
            catch (ConfigurationErrorsException)  
            {  
                Console.WriteLine("Error reading app settings");  
            }  
        }  
  
        static void ReadSetting(string key)  
        {  
            try  
            {  
                var appSettings = ConfigurationManager.AppSettings;  
                string result = appSettings[key] ?? "Not Found";  
                Console.WriteLine(result);  
            }  
            catch (ConfigurationErrorsException)  
            {  
                Console.WriteLine("Error reading app settings");  
            }  
        }  
  
        static void AddUpdateAppSettings(string key, string value)  
        {  
            try  
            {  
                var configFile = ConfigurationManager.OpenExeConfiguration(ConfigurationUserLevel.None);  
                var settings = configFile.AppSettings.Settings;  
                if (settings[key] == null)  
                {  
                    settings.Add(key, value);  
                }  
                else  
                {  
                    settings[key].Value = value;  
                }  
                configFile.Save(ConfigurationSaveMode.Modified);  
                ConfigurationManager.RefreshSection(configFile.AppSettings.SectionInformation.Name);  
            }  
            catch (ConfigurationErrorsException)  
            {  
                Console.WriteLine("Error writing app settings");  
            }  
        }  
    }  
}

using System;  
using System.Configuration;  
using System.Data.SqlClient;  
  
namespace ConsoleApplication1  
{  
    class Program  
    {  
        static void Main(string[] args)  
        {  
            ReadProducts();  
        }  
  
        static void ReadProducts()  
        {  
            var connectionString = ConfigurationManager.ConnectionStrings["WingtipToys"].ConnectionString;  
            string queryString = "SELECT Id, ProductName FROM dbo.Products;";  
            using (var connection = new SqlConnection(connectionString))  
            {  
                var command = new SqlCommand(queryString, connection);  
                connection.Open();  
                using (var reader = command.ExecuteReader())  
                {  
                    while (reader.Read())  
                    {  
                        Console.WriteLine(String.Format("{0}, {1}", reader[0], reader[1]));  
                    }  
                }  
            }  
        }  
    }  
}
