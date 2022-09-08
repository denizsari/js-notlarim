# Javascript-notlarim
Javascript öğrenme aşamasında derlediğim kişisel öğrenim notlarım.

//! Notlar

//todo Mini notlar
//! Temel JS Yazım Kuralları (Syntax)
//? JS 'case sensitive'(büyük-küçük harf duyarlı) bir dildir. (var degisken; -- alert(Degisken) hata verir).
//? JS komutları ; ile biter fakat bu opsiyoneldir. ; olmadan da kodlar çalışır.
//? document.getElementById('div').innerHTML = '<h1>Başlık</h1>'; JS kodları içerisine de html tagleri gömülüp çalıştırılabilir.


//todo Kod içerisinde ' kullanımı
//? 'Deniz\'in evi' Kod içerisinde ' işareti kullanmak için öncesinde \ kullanılması gerekir aksi takdirde kodu bozar.

//todo int + string değer
//? 10 + "21" % "21" + 10 olarak yazılan veri tipinin alacağı karşılık "1021" özetle int bir değer ile string bir değer toplanmak istenirse string olarak çıktı alınır.

//todo int - string değer
//? 10 - "31" % "31" - 10 olarak yazılan veri tipinin alacağı karşılık int/double/float olacaktır string ile sayısal bir değer çıkarılmaya çalışıldığınd sayısal değer olarak yansır.

// todo Değişkenler
//? Uygulama akışı içerisinde tutulan değerler ve değerlere ulaşılması ve tanımlanması.
//? Değişken tanımlarken rakamları, harfleri ve _ kullanabiliriz. Fakat değişken isimleri rakamla başlayamaz.
//? Bir değişken aynı anda sadece tek değer saklayabilir.

//? Değişken tanımlama.
var degisken1;

//? Aynı anda birden fazla değişken tanımlanabilir.
var degisken1, degisken_2;

//? Değişkene ilk değer ataması.
var isim = "Asya";

//? Değişken tanımlama ve değer atama.
var baslangic = 78,
  bitis = 90;

//? Değişken tanımlama ve değerini daha sonra atama.
var dogruMu;
dogruMu = false;

var notlar = "Deniz SARI"; //? notlar değişkeni çağrıldığında getireceği sonuç "Deniz SARI" olacaktır.
notlar = notlar + "İnsandır"; //? Notlar değişkenine sonradan eklenen değer "İnsandır". notlar = "Deniz SARI İnsandır"
notlar = prompt("Eğitmen Kim?"); //? Değişkene kullanıcıya bir pop up soru çıkararak sorunun cevabına göre atama yapılması.
//* notlar prompt atamasından daha sonra çağrıldığında kullanıcıdan gelen değer atanacaktır. notlar değişkeni tekrar çağrıldığında bu değer ile dönecektir.

// todo Boolean örnek
//* boolean true ve false değerleri ile bir döngü alır bu döngünün karşılığını size döndürür.
var dogruMu = true; //? Boolean mantıksal ifade atama
dogruMu(true); //? atanan ifadenin dönüşü.
//? var age1 = 18
//? var age2 = 19
//? age1 < age2 = true
//? age1 > age2 = false
//? 3>4 false - 3<4 true -- örnek  >
//? 3>=2 true 3<=2 false >= <=
//? 3==3 true 3==4 false ==
//? 3=="3" yapısal durum da metin ve sayı eşit olarak true aktarır == string int
//? 3===3 === olarak bakıldığında verinin türüne de bakarak veri türlerine göre sonuç döndürür === veri türüne göre döner
//? 3!==3 false = !== eşit değil mi ? (3!==4 true 3 4 eşit değildir) !== eşit değil mi ?

// todo Number() fonksiyonu
//? Number() fonksiyonu string değerlerin sayısal değerlere dönüştürülmesi için kullanılan fonksiyondur.
var sayi1 = prompt("Sayı 1 ?"); //? Kullanıcıdan talep edilen ilk değer ?
var sayi2 = prompt("Sayı 2 ?"); //? Kullanıcıdan talep edilen ikinci değer ?
var toplam = sayi1 + sayi2; //? Kullanıcıdan gelen 2 değerin bellekte tutulup toplanması için yapılan atama ?

//! toplam = sayi1 + sayi2 Çıkacak olan değer string bir ifade olarak dönecektir bu yüzden sayısal işlem amaçlı alınan değerlerde yapılması gereken alt kısımda ki gibidir.
var toplam = Number(sayi1) + Number(sayi2); //? Number() fonksiyonu metinsel ifadeleri sayısal ifadelere çevirerek işleme alır!

// todo Şart blokları İf Else
//! if ifadesi eğer anlamına gelir. Kullanım şekli; Eğer belirttiğim koşul yerine geliyorsa şunları, gelmiyorsa bunları yap demektir. else ifadesi ise; her iki koşulda yerine gelmiyorsa yapılacak işlemi belirtir.

var ögrenci = "Deniz Sarı"; //? Tanımlanan değişkenin verisi "Deniz Sarı".Burada tanımlanan veri ataması manuel atamadır bu atama sql veya benzeri database işlemleri veritabanından çekilecek data ile değişir sabit kalmaz.
var mezunOgrenci = "Deniz Sarı";
//? ögrenci değişkeninin kontrolü
if (ögrenci == mezunOgrenci) {
  //* Eğer öğrenci yukarıda atanan mezunOgrenci değişkenine eşit ise
  alert("Mezun Öğrenci " + ögrenci);
} else {
  //* Eğer öğrenci yukarıda atanan mezunOgrencı değişkenine eşit değil ise
  alert("Öğrenci Bulunamadı ");
}

//? ogretmen ve aktifOgretmen olarak atanan iki değer.
var ogretmen = "Deniz SARI";
var aktifOgretmen = "Mustafa Kemal ATATÜRK";
if (ogretmen == aktifOgretmen) {
  alert("Öğretmen " + aktifOgretmen);
} else {
  alert("Şuan ki öğretmen" + aktifOgretmen + " Değil");
}

//? prompt() içerikli örnek
var sonuc = "Deniz Sarı"; //? Sonuç olarak atanmış değer.
var ara = prompt("Ara ? "); //? ara içerisine kullanıcı cevabı ile atanacak olan değer eğer sonuc değerine eşit işe console üzerinde sonuc değeri gözükecektir.
if (ara == sonuc) {
  alert(sonuc);
} else {
  alert("Sonuç bulunamadı!");
}

//! if else şart blokları
//* isim değişkenine atanan isim eğer Deniz veya Derin veya Ahmet ise alert çalışacaktır fakat ikiside değilse kod çalışmayacaktır.

var isim = "Deniz";
if (isim == "Deniz") {
  //? Eğer isim Deniz ise çalışacak olan alert
  alert("İsim = " + isim);
} else if (isim == "Derin") {
  //? Eğer isim Derin ise çalışacak olan alert
  alert("İsim = " + isim);
} else if (isim == "Ahmet") {
  //? Eğer isim Ahmet ise çalışacak olan alert
  alert("İsim = " + isim);
} else {
  //? hiçbiri değil ise çalışacak olan alert
  alert("Tanımıyorum");
}

//* || "veya" şartının kullanımı
var ogrenci = "Deniz";
if (ogrenci == "Deniz" || ogrenci == "Derin") {
  //? Eğer öğrenci adı Deniz veya Derin ise çalışacak olan alert
  alert("Öğrenci İsmi = " + ogrenci);
} else {
  //? Eğer öğrenci adı Deniz veya Derin değil ise çalışacak olan alert
  alert("Bulunamadı");
}

//* && "ve" şartının kullanımı
var ogrenciAdi = "Deniz";
var ogrenciSoyadi = "Sarı";
if (ogrenciAdi == "Deniz" && ogrenciSoyadi == "Sarı") {
  //? Eğer ogrenciAdi Deniz ogrenciSoyadi Sarı ise çalışacak olan alert
  alert("Öğrenci İsmi = " + ogrenciAdi + " " + ogrenciSoyadi);
} else {
  //? Eğer ogrenciAdi Deniz ogrenciSoyadi Sarı değil ise çalışacak olan alert
  alert("Bulunamadı ");
}

// todo Obje oluşturma ve kullanma
//! Objeler, içerisinde birden farklı veri türünü içeren, yazılımcı tarafından oluşturulan daha komplike veri türleridir. İçerisinde farklı veri türleri tutabildiği gibi, farklı objeleri de tutabilmektedir.

//* Obje Oluşturma
//? gamer adında ki oluşturulan obje ve içerisinde ki veriler
var gamer = {
  gamerName: "Emin Ali",
  gamerNumber: 313131,
  gamerWeapon: ["R301", "Car"],
};

//? gamer objesinden çekilen 3 farklı veri ve çıktısı
console.log(gamer.gamerName);
console.log(gamer.gamerNumber);
console.log(gamer.gamerWeapon);

//? İç İçe Obje Oluşturma (Nested Objects)
var newGamer = {
  //? oluşturulan Obje
  newName: "Erkan", //? objede bulunan name verisi.
  newNumber: 696969, //? objede bulunan number verisi.
  newWeapon: ["R301", "Car"], //? objede bulunan weapon verisi.
  newInfo: {
    //? newGamer içerisinde oluşturulan yeni obje.
    age: 24,
    gender: "male",
  },
};

console.log(newGamer.newName); //? newGamer objesinin içerisinde ki bulunan newName verisi.
console.log(newGamer.gamerNumber); //? newGamer objesinin içerisinde ki bulunan gamerNumber verisi.
console.log(newGamer.newInfo.age); //? newGamer objesinin içerisinde ki bulunan newInfo objesinden çekilen age verisi.

//* Obje İçerisinde Fonksiyon Oluşturma

var customer = {
  name: "Deniz",
  surname: "Sarı",
  number: 313131,
  customerInfo: function () {
    //? Obje içerisinde fonksiyon oluşturma ve çağırma. Burada "This" anahtar sözcüğü devreye girmektedir. Bu keyword obje içerisindeki değişkenin kullanılması gerektiğini belirtir.
    return "İsim: " + this.name + " Soyisim: " + this.surname; //? Return komutu, bir fonksiyonun sonlandırılmasına ve fonksiyonun çağırıldığı yere değer götürmesine yarar.
  },
};

console.log(customer.customerInfo());

//* Farklı yöntemler ile obje oluşturma

function Employee(name, surname, number) {
  //? Yapıcı metot
  this.name = name;
  this.surname = surname;
  this.number = number;
  this.showInfo = function () {
    //? metot içerisinde fonksiyon.
    return (
      "Name: " +
      this.name +
      "\nSurname: " +
      this.surname +
      "\nNumber: " +
      this.number
    );
  };
}

var employee1 = new Employee("Turan", "Blade", 454535); //? yeni obje oluşturulması bu değişkende atanan veriler objede ki değişkenlerin karşılığı olacaktır.
var employee2 = new Employee("Hebele", "Hübele", 324353); //? başka bir obje oluşturulması bu değişkende atanan veriler objede ki değişkenlerin karşılığı olacaktır.

console.log(employee1.showInfo()); //? oluşturulan employee1 objesinin içerisinde ki bulunan showInfo fonksiyonunun verisi.
console.log(employee2.showInfo()); //? oluşturulan employee2 objesinin içerisinde ki bulunan showInfo fonksiyonunun verisi.

if (employee1.name == "Deniz") {
  //? Oluşturulan employee1 objesinden name verisini çekme.
  alert("Dogrulandı");
}

// todo Fonksiyonlar

//! Basit örnekler

function selamVer() {
  //? selamVer adı ile oluşturulan fonksiyon console üzerinde bir Merhaba yazmak ile görevlendiriliyor.
  console.log("Merhaba");
}

selamVer(); //? Yukarıda oluşturulan bu fonksiyon çağrıldığında console üzerinde bir Merhaba çıkacaktır.

function game() {
  var engineSearch = prompt("Nedir ? ");
  var engineName = "Apex Legends";

  if (engineSearch == engineName) {
    console.log("Oyun " + engineName);
  }
}

game();

//? Yukarı da ki fonksiyonlarda ki amaç bir veriyi ve bu veri içinde ki döngüyü bir fonksiyon içerisinde tutup gerektiği yerde çağrılması.

//? Altta ki topla fonksiyonun a ve b bir parametre veya argümandır.

function topla(a, b) {
  return a + b;
}

var rakam = prompt("İlk Rakam Nedir ? "); //? Örnek olması için oluşturulan bu veri de kullancıdan ilk rakam talep ediliyor.
var digerRakam = prompt("İkinci Rakam Nedir ? "); //? Örnek olması için oluşturulan bu veri de kullancıdan ikinci rakam talep ediliyor.

var sonuc = topla(Number(rakam), Number(digerRakam)); //? sonuc verisinde ise yukarıda kullanıcıdan gelen iki veri Number() ile sayısal değere döndürülüp verisi tutuluyor ve çağrıldığında bu iki verinin toplamını bizlere yazıyor.

// todo Array / Diziler

var numbers = [1, 3, 5, 7, 8, 11]; //? dizinin ilk elemanı olan 1 in index numarası 0'dır 0 dan başlar 5 e kadar devam eder (6 adet sayı bulunmakta).

var dizi = ["Ankara", 1, false]; //? Bir dizi içerisin de 3 farklı veri tipi barındırmak mümkündür çağrılan indexe göre veri aktarılır.

var fonksiyonDizisi = [
  function selamVer() {
    console.log("Birinci Fonksiyon Çalıştı");
  },
  function selamVer2() {
    console.log("İkinci Fonksiyon Çalıştı");
  },
];

//* Eğer fonksiyonDizisi[1] çağrılır ise dizi 2. dizi de ki fonksiyon elemanını bize gösterir
//* Eğer fonksiyonDizisi[1]() olarak çağrılır ise fonksiyonDizisi'ne ait 2. fonksiyonun içerisinde ki fonksiyon çalıştırılır.

// todo Dizi Fonksiyonları

var sehirler = ["Ankara", "İstanbul", "İzmir"];

sehirler.pop(); //* pop çağrılan dizinin son elemanını diziden çıkarır ve size hangi veri olduğunu gösterir.
sehirler.shift(); //* pop fonksiyonun tam tersi olarak en başta ki elemanı alır ve diziden çıkarır.
sehirler.push("Bursa"); //* push İçerisinde ki veriyi dizi'nin son indexi olarak diziye ekler.

sehirler.concat(["Van", "Muş"]); //* sehirler dizisine birleştirir ve bize veriyi gösterir ama DİZİYE EKLEMEZ.
sehirler.sort(); //* sehirler dizisini alfabetik olarak sıralar.
sehirler.length; //* sehirler dizisinin elemanın sayısını verir.

// todo For While forEach

//*for yapısı
for(başlangıç değeri ; koşul ; artış miktarı)
{
    //?kodlar
}


//* For döngüsü
for (i = 1; i <= 10; i++) {
  //? i = 1; i <=10, i++ i eşitse 1e 1 küçükse veya eşitse 10 dan iye ekleyerek devam et ta ki i 10 a eşit olana kadar.
  console.log(i);
}

var sehirler = ["Ankara", "İstanbul", "İzmir", "Adana"]; //? Şehirler dizisi.

for (i = 0; i < sehirler.length; i++) {
  //? eğer i sehirler dizisinin uzunluğundan kısa ise iye ekleyerek devam et ta ki i sehirlerin uzunluğuna eşit olana kadar.
  console.log(sehirler[i]); //? sehirler dizisi ekrana sırası ile yazdırılır.
}

//* While döngüsü
var i = 1; //? fordan farklı olarak i yi burda bir veri olarak sabitliyoruz.

while (i < 10) {
  //? burda bir şart koşuyoruz ve diyoruz ki eğer i küçükse 10dan (i = 1).
  console.log(i); //? i nin değerini ekrana yazdırıyoruz fakat eğer bir alt satırda ki kod eklenmez ise sonsuza kadar bu döngü devam edecektir!
  i++; //? i ye ekleme yapıyor ta ki 10 dan büyük olana kadar eğer yapılmazsa döngü sonsuza kadar devam eder.
}

var i = 1;

do {
  console.log(i);
  i++;
} while (i < 10);

//* forEach kullanımı

//? sayilar isminde bir dizi oluşturalım .
var sayilar = [1, 2, 3, 4, 5, 6, 7];

//? Şimdi bu oluşturduğumuz sayilar dizisini foreach ile konsola yazdıralım.
sayilar.forEach(function (item) {
  console.log(item);
});

//? Browser konsolda aşağıdaki gibi bir çıktı göreceksiniz .
//* 1;
//* 2;
//* 3;
//* 4;
//* 5;
//* 6;
//* 7;

//* eğer yukarıdaki fonksiyonu şu şekilde yazmış olsaydık

sayilar.forEach(function (item, index, array) {
  console.log(item, index, array);
});

//? Bu yazım şeklinde browser konsolda aşağıdaki gibi bir çıktı göreceksiniz .
//* 1 0 [1,2,3,4,5,6,7]
//* 2 1 [1,2,3,4,5,6,7]
//* 3 2 [1,2,3,4,5,6,7]
//* 4 3 [1,2,3,4,5,6,7]
//* 5 4 [1,2,3,4,5,6,7]
//* 6 5 [1,2,3,4,5,6,7]
//* 7 6 [1,2,3,4,5,6,7]



//* for in kulanımı
//? `for in` ile nesne içindeki özellikler kadar döngüye girilir.

var film = {isim:"Matrix", tur:"Bilim Kurgu", yil:2500};
var x;
for (x in film) {
    console.log(film[x]);
}

//? Yukarıdaki örnekte film nesnesi içindeki her bir özellik için döngü çalışacak ve konsola Matrix, Bilim Kurgu, 2500 yazılacaktır.

// todo DOM Manipulasyonu

//* HTML içerisin de ki divlerin veya yapıların idleri aracılığı ile innerHTML kısmına müdahale edebildiğimiz fonksiyondur.
<p id="bio">innerHTML</p>; //? Js kodu çalıştığında değişecek olan html kodu
document.getElementById("bio").innerHTML = "Deniz Sarı 1999"; //? Js kodu çalıştığında bio idsine sahip olan <p> tagı js içerisinde innerHTML komutunda belirtilen değeri alacaktır.

//* documents.getElementByTagName kullanım örneği
var tumListeler = document.getElementsByTagName("ul"); //? ul tagını tumListeler değişkenine atıyoruz.
var sehirler = tumListeler[0]; //? tumListeler olarak tanımlanan ul tagına ait divlerden hangisi üzerinde çalışmak istediğimizi belirttiğimiz değişken.

tumElemanlar = sehirler.getElementsByTagName("li"); //? ul tagının altında ki liste elemanlarının değişkeni.

//! yukarıda ki değişkenlerin sırasıyla alertlenmesi için gereken for döngüsü
for (i = 0; i < tumElemanlar.length; i++) {
  alert(tumElemanlar[i].innerHTML); //? yukarıda tanımlanan değişkenin veri olarak çektiği "li" tagının içerisinde ki html verilerinin for döngüsü ile index edilmesi.
}

//* documents.getElementsByClassName kullanım örneği
//! getElementsByClassName merhodu ile yakaladığımız elemanların değerlerini elde edebilir veya istediğimiz değeri ekleyebilir, güncelleyebiliriz.

<p class="simple"> Hello World </p>;

var e = document.getElementsByClassName("simple");
console.log(e[0].innerHTML);

//! Class işlemlerinde id değeri gibi tek bir değer yerine sayfa içerisinde aynı class değerine sahip tüm elemanları seçmektedir. Bu nedenle getElementsByClassName methodu bizlere list olarak geri dönmektedir.
//! ulaşmak istediğimiz html elemanına index numarası ile elemana ait değerleri elde edebilmekteyiz.

//* querySelectorAll kullanım örneği
//! Javascript querySelector kullanımında Jquery deki seçiciler gibi az kodla çok iş yapmamıza olanak sağlamaktadır. Tek bir seçici ile id, class veya direk etiketi seçme işlemi sağlayabilmekteyiz.

//!Etiket seçimi :

<p> Hello 1</p>;

var e = document.querySelector("p"); //? p tagını kullanan tüm documentleri seçer.
e.style.color = "red";

//! Div seçimi :

<div id="blok"> Hello 2</div>;

var e = document.querySelector("#blok"); //? blok divini kullanan tüm divleri seçer.
e.style.color = "blue";

//! Class seçimi

<h4 class="baslik"> Hello 3</h4>;

var e = document.querySelector(".baslik"); //? baslik classını kullanan tüm classları seçer.
e.style.color = "orange";

//! Yukarıdaki örneklerde sırasıyla etiket, div ve class değerleri iler nesneler üzerinde seçim işlemi sağlanmıştır.

//* getElementsByName kullanımı

<input type="text" name="musteriAdi" value="Deniz Sarı"></input>; //? html tarafında belirlenen name ile açılan input.

var musteriAdi = document.getElementsByName("musteriAdi"); //? js tarafından bu name değerini kullanan verileri değişkene atama.

alert(musteriAdi[0].value); //? atanan değişken içerisinde ki name değerini kullanan html verisinin value bilgisine erişme ve alert ile belirtme.

//* AddEventListener kullanımı
//! JavaScript addEventListener yöntemi, bir kullanıcı bir düğmeyi tıkladığında olduğu gibi, belirli bir olay gerçekleştiğinde çağrılacak işlevleri ayarlamanıza olanak tanır. Olaylar, kullanıcı veya tarayıcı bir sayfayı manipüle ettiğinde gerçekleşen eylemlerdir.
var deniz = document
  .getElementById("deniz") //? id si deniz olan html verisi çekiliyor.
  .addEventListener("click", rengiDegistir); //? bu id ile belirlenen veriye mouse ile tıklandığında çalışması istenilen fonksiyon.

function rengiDegistir() {
  //? id si deniz olan html verisi çekiliyor.
  document.getElementById("div1").style.color = "red"; //? fonksiyon çalıştığında div1 id sine ait divin text rengi kırmızı oluyor.
  var isimElemanları = document.getElementsByName("musteriAdi"); //? daha önce belirlenen input değeri değişkene atanıyor.
  isimElemanları[0].value = "Emin"; //? atanan input değerinin value değeri fonksiyon ile birlikte değişiyor.
}

// todo Nodlarla çalışmak

var baslik = document.createElement("h2");
var node = document.createTextNode("Merhaba Javascript");
baslik.appendChild(node);

var deniz = document.getElementById("deniz").addEventListener("click", ekle);

function ekle() {
  var div1 = document.getElementById("div1");
  var p2 = document.getElementById("p2");
  div1.insertBefore(baslik, p2);
  div1.removeChild(p2);
}
