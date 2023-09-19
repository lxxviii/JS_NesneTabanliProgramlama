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

##### constructor            : Object'in oluşturduğu yapıcı metoda (işleve) erişmek için kullanılan özelliktir.  
##### __proto__              : Object'i oluşturan prototype object'ini elde etmek için kullanılan özelliktir.
##### hasOwnProperty         : Bir object'in parametrik olarak girilen özelliğinin kullanılıp kullanılmadığını test etmek için kullanılır.
##### isPrototypeOf          : Parametrik olarak verilen object'in prototype zincirinde, bir constructor'ın bulunup bulunmadığını test etmek için kullanılır.
##### unwatch                : Belirtilen bir özelliğin değeri değiştirdiğinde, eklenmiş olan herhangi bir işlevi kaldırmak için kullanılır.
##### propertyIsEnumerable   : Bir object'in parametrik olarak girilen özelliğinin kullanılıp kullanılmadığının ve bu özelliğin numaralandırılabilir olup olmadığını test etmek için kullanılır.
##### toLocaleString         : Bir object'in karakter dizesi olarak temsil eden halini döndürmek için kullanılır. (Location)
##### toString               : Bir object'in karakter dizesi olarak temsil eden halini döndürmek için kullanılır. (No Location)
##### toSource               : Bir object'in kaynak kodunu temsil edene halini döndürmek için kullanılır.
##### valueOf                : Bir object'in temel değerini elde etmek için kullanılır.
##### watch                  : Belirtilen bir özelliğin değeri değiştiğinde, çalıştırılacak herhangi bir işlevi eklemek için kullanılır.
