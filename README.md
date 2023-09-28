 #### JS_NesneTabanliProgramlama

    var bilgiler = { isim:"Name" }; //Standart Kullanım

    var bilgiler = new Object(); // Alternatif Kullanım, creating object
    bilgiler.isim = "Name";    //creating object.bilgiler.isim and set valueOf "Name"

    var bilgiler = new Object(); //
    bilgiler["isim"] = "Name"; //Alternatif Yöntem

    function objeyeAtanacakFonksiyon () {
      this.isim = "Name";
      }
    var bilgiler = new objeyeAtanacakFonksiyon();

    var objeyeAtanacakFonksiyon = function() {
        this.isim = "Name";
        }

    For In : var bilgiler = { isim : "isim", soyisim:"soyisim" }

    for (let sonuc in bilgiler) // isim isim soyisim soyisim => [] //Eğer bir fonksiyon varsa onun içindeki değerleri dönüyor. 
    {
        if(sonuc !== "fonksiyonKey") { let ozellik = sonuc; let deger = bilgier[sonuc]; document.write(ozellik + " " + deger); } 
    }

    PROTOTYPE : funciton bilgiler (birinciDegisken, ikinciDegisken, ucuncuDegisken) 
    { 
    this.birinciDegiskeKendisi = birinciDegisken; this.ikinciDegiskenKendisi = ikinciDegisken; this.ucuncuDegiskenKendisi = ucuncuDegisken; 
    }
    bilgiler.prototype.islem = function() 
    { 
    return this.birinciDegiskeKendisi + this.ikinciDegiskenKendisi + this.ucuncuDegiskenKendisi; 
    } 
    var sonuc = new bilgiler("Birinci Değişken", "İkinci Değişken", "Üçüncü Değişken"); 
    var yazdir = sonuc.islem(); 
    document.write(yazdir);

##### constructor            : Object'in oluşturduğu yapıcı metoda (işleve) erişmek için kullanılan özelliktir. 
                               // Nesnenin constructor'ını elde etmek için kullanılır ve constructor'ın değerini döndürür. Ayrıca aynı zamanda kontrol işlemleri içinde kullanılabilir.

                               function bilgiler() { isim:"ISIM"; }
                               var sonuc = new bilgiler();
                               var islem = sonuc.constructor; 
                               document.write(islem);  

##### __proto__              : Object'i oluşturan prototype object'ini elde etmek için kullanılan özelliktir. 
                               //Bir nesnenin prototype nesnesini elde etmek için kullanılır ve prototype nesnesi içerisindeki değere ulaşarak değeri geriye döndürür

                                function bilgiler() {
                                    this.isim = "ISIM";
                                    this.soyad = "SOYAD";
                                    }
                                    
                                funciton.protype.bilgiler = function() 
                                    {
                                    this.ifade = "Merhaba";
                                    }
                                var sonuc = new bilgiler();
                                sonuc.__proto__.islem();  //nesnenin proto'suna ilaşmak için değere ulaşmadan önce çalıştırmak gerekir.
                                
                                var ifadeYaz = sonuc.__proto__.ifade; 
                                document.write(ifadeYaz);



##### hasOwnProperty         : Bir object'in parametrik olarak girilen özelliğinin kullanılıp kullanılmadığını test etmek için kullanılır. //true - false
                              var bilgiler= {
                                  isim = "ISIM"; soyad="SOYAD";
                              }
                              var isimKontrolet = bilgiler.hasOwnProperty("isim"); //true
                              document.write("isimKontrolet");

##### isPrototypeOf          : Parametrik olarak verilen object'in prototype zincirinde, bir constructor'ın bulunup bulunmadığını test etmek için kullanılır.

                              var sonuc = new bilgiler();
                              var kontrolEt = bilgiler.prototype.isPrototypeOf(sonuc); //true - false

##### unwatch                : Belirtilen bir özelliğin değeri değiştirdiğinde, eklenmiş olan herhangi bir işlevi kaldırmak için kullanılır.
                               // Sadece Mozilla'da çalışır.   degisken.unwatch("object.ozelligi");
                               
##### propertyIsEnumerable   : Bir object'in parametrik olarak girilen özelliğinin kullanılıp kullanılmadığının ve bu özelliğin numaralandırılabilir olup olmadığını test etmek için kullanılır. 
                              //true - false && numaralandırılıp numaralandırılamayacağını(işlem sırası) kontrol eder

                                function bilgiler() {
                                    this.isim = "ISIM";
                                    this.soyad = "SOYAD";
                                    }
                                    
                                funciton.protype.bilgiler = function() 
                                    {
                                    this.ifade = "Merhaba";
                                    }
                                var sonuc = new bilgiler();
                                sonuc.__proto__.islem();  //nesnenin proto'suna ilaşmak için değere ulaşmadan önce çalıştırmak gerekir.
                                
                                var ifadeYaz = sonuc.__proto__.ifade; 
                                document.write(ifadeYaz);
                 
##### toLocaleString         : Bir object'in karakter dizesi olarak temsil eden halini döndürmek için kullanılır. (Location)  
                                      var deger = 1000; var sonuc = deger.toLocaleString ("tr-TR", { style:"currency", currency:"TRY", maximumSignificantDigits: Deger }); 
                                      // Deger = Maximum alabileceği değer sayısını girer. En fazla 21 karaktere kadar alabilir.

                                      var deger = 1000; var sonuc = deger.toLocaleString ("tr-TR", { style:"currency", currency:"TRY", minimumSignificantDigits: Deger });
                                      // Deger = Minimum alabileceği değer sayısını girer.  En fazla 21 karaktere kadar alabilir. --Minimum karaktere ulaşılamazsa virgülden sonra sıfır ekler.--

##### toString               : Bir object'in karakter dizesi olarak temsil eden halini döndürmek için kullanılır. (No Location)
#####                          Nesne prototype özelliği kullanarak değer ataması yapılabilir.
                                     function islem() { document.write("Text Mesajı");  }
                                     islem.prototype.toString = function() { document.write("Diğer Text Mesajı"); }
                                     var bilgiler = new islem();
                                     var sonuc = bilgiler.toString();

##### toSource               : Bir object'in kaynak kodunu temsil edene halini döndürmek için kullanılır.
                               // Sadece Mozilla'da çalışır. 

##### valueOf                : Bir object'in temel değerini elde etmek için kullanılır.
                               function islem(sayi){ this.deger = sayi; }
                               var nesnemi = new islem(50);
                               var sonuc = nesnemiz.valueOf();
                               document.write(sonuc);

##### watch                  : Belirtilen bir özelliğin değeri değiştiğinde, çalıştırılacak herhangi bir işlevi eklemek için kullanılır.
                               // Sadece Mozilla'da çalışır.  degisken.watch("object.ozelligi", "ozellikAdi, eskiDeger, yeniDeger") {  -- çeşitli işlemler -- };

#####instanceof              : Bir nesnenin constructor'ının doğruluğunu kontrol ederek boolean veri türünde sonucu geriye döndürür.

                               function demobir() { }
                               function demoiki() { }
                                 
                               var sonucbir = new demobir();
                               var islemInstanceof = sonucbir instanceof demobir; //true - false
                               document.write(islembir);

Değişken içindeki Veriyi Silmek için : delete degisken;
