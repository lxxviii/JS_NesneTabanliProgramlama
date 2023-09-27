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

##### __proto__              : Object'i oluşturan prototype object'ini elde etmek için kullanılan özelliktir. 
                               (Bir nesnenin prototype nesnesini elde etmek için kullanılır ve prototype nesnesi içerisindeki değere ulaşarak değeri geriye döndürür)

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
##### unwatch                : Belirtilen bir özelliğin değeri değiştirdiğinde, eklenmiş olan herhangi bir işlevi kaldırmak için kullanılır.
##### propertyIsEnumerable   : Bir object'in parametrik olarak girilen özelliğinin kullanılıp kullanılmadığının ve bu özelliğin numaralandırılabilir olup olmadığını test etmek için kullanılır. ( //true - false && numaralandırılıp numaralandırılamayacağını kontrol eder)

                 
##### toLocaleString         : Bir object'in karakter dizesi olarak temsil eden halini döndürmek için kullanılır. (Location)
##### toString               : Bir object'in karakter dizesi olarak temsil eden halini döndürmek için kullanılır. (No Location)
##### toSource               : Bir object'in kaynak kodunu temsil edene halini döndürmek için kullanılır.
##### valueOf                : Bir object'in temel değerini elde etmek için kullanılır.
##### watch                  : Belirtilen bir özelliğin değeri değiştiğinde, çalıştırılacak herhangi bir işlevi eklemek için kullanılır.

Değişken içindeki Veriyi Silmek için : delete degisken;
