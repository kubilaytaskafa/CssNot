# CssNot
Kendi tuttuğum css notlarıdır.



            -css söz dizimi ve örnek buton yapımı DERS  1-

css söz dizimi:
seçici{property(css özellikleri):değeri;property:değeri}   şeklindedir.

seçici hangi elemente işlem yapacağımızı belirtir.
css işaretlemeleri {} içerisine yazılır.
property   kullanacağımız css özelliğidir. color gibi 
değer ise vermek istediğimiz property değeridir. örneğin color red gibi

örnek uygulama:
<style>
    button{    butonumuzu seçtik 
        color: red;   buton içindeki yazı reengi kırmızı olacak
        background-color: black;  butonumuzun arka plan rengi siyah olacak
    }
</style>

<button>katıl</button>

!cs özelliği ne ise sol tarafa : değeri ne ise sağ tarafa yazılır.
örnek=  backgorund-color:red  


şimdi sizlerle beraber bir css buton uygulaması yapacağız.

uygulama:
<style>
  button {
    color: #3ea6ff; /* seçili elementin yazı rengini belirler*/
    background-color: rgb(
      0,
      0,
      0
    ); /* seçili elementin arka plan rengini belirler*/
    border: 1px solid #3ea6ff; /*seçili elementin kenarlık özelliklerini belirler 1px kalınlığında solid düz çizgi ve renk*/
    width: 72px;  /* seçili elementin genişliğini belirler*/
    height: 37px; /*seçili elementin yüksekliğini belirler*/
  text-transform: uppercase; /* seçili elementin içindeki yazıların büyük küçük olma durumunu belirler*/
 border-radius: 2px;  /*seçili elementin kenar keskinliğini belirler*/
 cursor: pointer; /*seçili elementin üzerine gelindiğinde fare imlecimiz tıklanabilir olur.*/
 }
</style>

bizler renk kullanımında rgb de kullanırız.
rgb red green blue demektir. bu değerler 0 ile 255 arasında değerler alarak farklı renkler oluşturur.
bizler tam renkleri bulmak için rgb değerleri vererek renk buluruz.
örnek kullanım = background-color: rgb(0,0,0);
burada red green blue değerlerine 0 verirsek siyah rengini buluruz.

bizler web site oluştururken önce html i yazar sonra css i yazarız.

bizler elementleri classlara ve idlere bağlarsak daha iyi bir seçim ve işaretleme yapabiliriz.
classlar ile  birden fazla elemente aynı özellikleri verebilirsiniz.
id ye sadece bir tane element bağlanır. eşsiz öellikleri kullanmak için elementi bir id ye bağlayabilirisiniz.

classlar . ile seçilir   örnek:
.item-group{
}

id ler # ile seçilir  örnek:

#para1{

}

  
       
       
          - CSS HOVER TRANSİTİONS VE SHADOWS DERS 2-

*hover:
bir html etiketinin üzerine gittiğimizde olması gereken kodları yazacağımız seçicidir.
kullanımı: 
örnek element,class,id :hover{

}
şeklindedir.

örnek:
 
   button:hover{
        color: white;
    }
    burada butonumuzun üstüne geldiğimizde buton içindeki yazı rengi beyaz olacak

uygulamalı örnek:

<style>
    button{
        background-color: #04aa6d;
        border: none;
    }
    button:hover{
        color: white;
        background-color: red;
    }

</style>



<button>kaydol</button>

buton arka plan rengimiz ve border özelliğimiz işaretlendi.
buton hover durumunda iken yani buton üzerine geldiğimizde color backgorund color özellikleri değişecek
yani hover durumunda ne işaretlendiyse element o duruma gelecek 

*transition:
geçiş hızını ve özelliklerini ayarlamaya yarar.

kullanımı:

element{
  transition:  ;
}
burada önemli olan transition u hangi özellikte kullanacaksanız onu eklemeniz.
örnek olarak bir elementin hover durumunda witdh değeri artıyor.
biz bu artışın süresini ayarlamak istiyorsak transition da witdh değerini eklememiz gerekir.

örnek:

<style>
    button{
        background-color: #04aa6d;
        border: none;
        width: 100px;
        *transition: width 2s;*
    }
    button:hover{
        color: white;
        background-color: red;
        width: 300px;
    }

</style>

!eğer bütün özelliklerin transition dan etkilenmesini istiyorsak:
transition:all 2s;  diyebiliriz.


*SHADOWS:
hmtl elementine gölge vermek için kullanılır.
kullanımı:

element{
  box-shadow: sağ aşağı tüm her yerden renk:
  }

örnek:
    button{
        background-color: #04aa6d;
        border: none;
        width: 100px;
        transition: width 2s;
        box-shadow: 10px 10px 5px red ;
    }
 ilgili elementin:
 10px genişliğinde sağdan:
 10px genişliğinde alttan
 5px genişliğinde her yerinden 
 bir gölge oluşturacak ve rengi kırmızı olacak

! shadowda sağ (right) ve aşağı(bottom) değerlerini - li verirsek:
right - ile left olur.
bottom - ile top olur.

        -CSS DEVTOOLS VE BOX MODEL DERS 3-
css kullanırken dev tools u çok fazla kullanacağız.
dev tools geliştirici panelidir.
taraıyıca f12 tuşu ile dev toolsa erişebilirsiniz.

paneldeki elements bölümünden sayfanın html etiketlerine ulaşabilirsiniz.
panelin sağ kısmındaki styles bölümünden seçili elementin style özelliklerine bkaabilirsiniz.geçici stiller verebilirsiniz.
refresh olduğunda verilen geçici stiller kaybolur.
computed kısmında seçili elementin margin padding değerlerini görebilirsiniz.

margin = bir elementin sağı solu üstü altından uzaklaşmasını sağlar.
elementlerin dıştaki boşluklarnı ayarlarız. elementleri seçtiğimizde etrafındaki sarı çizgiler
margin-rigt=sağ
margin-left=sol
margin-top=üst
margin-bottom=alt  kısımlarda boşluk bırakma kodudur.
px rem vb şeylerle boşluk bırakılır.


padding= element içerisindeki boşluklardır.  
örnek olarak bir div içerisindeki diğer elementlerine padding değeri vererek
div içerisindeki boşluklarını ayarlayabiliriz.
padding-rigt=sağ
padding-left=sol
padding-top=üst
padding-bottom=alt  kısımlarda boşluk bırakma kodudur.


paddingte kapsayıcı elementin witdh ve heigt özelliklerini aşamazsınız.



                -CSS TEXT STİLLENDİRME DERS 4-
ÖZELLİKLER:

1- FONT SİZE İLE YAZI BOYUTUNU BÜYÜTÜP KÜÇÜLTEBİLİRİZ.



2- FONT-WEİGHT= YAZI KALINLIĞINI PX VEREREK AYARLARIZ. 100 İLE 700 ARASINDA DEĞER VERİLEBİLİR.
BOLD DEDİĞİMİZDE EN KALIN YAZI STİLİNİ ALIRIZ.

3- FONT-STYLE= FONTUN STİLİNİ DEĞİŞTİREBİLİRİZ.
İTALİC DEĞERİ İLE İTALİC STİLİ KULLANIRIZ.

4- TEXT-DECORATİON:UNDERLİNE İLE TEXTİN ALTINI ÇİZEBİLİRİZ.

5- COLOR =TEXTİN RENGİNİ DEĞİŞTİREBİLİRİZ.

6-FONT-FAMİLY= YAZI AİLESİNİ DEĞİŞTİREBİLİRİZ ARİAL ROBOTO GİBİ 

7=LİNE-HEİGT= SATIR YÜKSEKLİĞİNİ AYARLAYABİLİRİZ.

8-LETTER-SPACİNG=HARFLERİN ARASINDAKİ BOŞLUKLARI AYARLAYABİLİRİZ.

9-TEXT-ALİGN= TEXTİ BAŞTA ORTADA SONDA KONUMLANDIRABİLİRİZ.
ÖRNEK UYGULAMA:

<style>
    p{
        font-size: 40px;
        font-weight: bold;
        font-style: italic;
        color: red ;
        text-decoration: underline;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
        line-height: 1.5;
        letter-spacing: 10px;
        text-align: center;
    }
</style>

<p>
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda earum
  asperiores fugiat, eum at dolorum beatae ipsum est, nostrum, odio repudiandae
  eligendi quibusdam consequatur? Eum explicabo itaque quos! Praesentium, nulla.
</p>

! w3schools/css_text  adresinden css text kaynaklarına ulaşabilirsiniz.



            
                                
                                -CSS İMAGE DERS 5-

bu dersimizde bir hmtl iskeleti oluşturacağız. 
html dosyası içerisinde !+enter yaparak html iskeleti oluşturabiliriz.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>

bu bizim hmtl iskeletimizdir.

resimlerimizi unsplash.com dan tedarik edebiliriz.


object-fit=
ilgili resim witdh ve heigt değerlerine göre bozulma yaşıyorsa 
object-fit ile bu durumu düzeltebiliriz.

object-fit değerine contain verirsek:
resim witdh we heigth değerlerine sığdırılır. fakat resmin witdh ve height değerine göre sığdırılır
geri kalan kısım boş kalır.

object-fit değerine cover verirsek:
tam olarak belirlenen witdh ve height değerlerine göre sığdırılır.
fakat resim tam olarak oturmayabilir.


object-position= bu özellik ile resmimizi kapsayıcı alan içerisinde konumlandırabiliriz.
örneğin top değeri verirsek resim kapsayıcı alanda üstte gözükür.
bottom aşağı alır.

eğer object-fit değeri cover ise object-position ile resmin hangi ksımının gözükeceğini ayarlayabiliriz.
örneğin kapsayıcıya sığmayan büyük bir resmin hangi bölümünün kapsayıcı içerisinde gözükeceğini ayarlayabiliriz.

w3schools.com/css_image kaynağından yararlanabilirsiniz.

!
backgorund-image:(RESİM URLSİ ); ÖZELLİĞİ İLE İSTEDİĞNİZ ETİKETİN ARKAPLANINA RESİM EKLEYEBİLİRSİNİZ.
backgorund-position ile de arkaplandaki resmin konumlandırmasını yapabiliriz.


                         
                            -CSS DİSPLAY DERS 6-
display html etiketleirmizin genişlik yükseklik,konumlandırmalarını değiştiren özelliktir.

display özellikleri:
block = block etiket bulunduğu bütün satırı kaplar. yani block bir etiketin yanına bir etiket daha gelmez.
eklenen etiket bir alt satıra gelir.

inline= inline etiket sadece kendisi kadar yer kaplar. inline etiketlerin yanına başka bir etiket eklenebilir.

!block ile inline arasındaki fark :
block element yanına element almaz inline alır.
inline element witdh height padding değeri almaz block alır.

block-inline= block-inline ile bir elementi hem inline hem de block özelliklerini verebiliriz.
örneğin inline bir element witdh ve height değeri almaz bu yüzden inline etiketleri inline-block yaparak witdh height verebiliriz.
inline-block ile bir elementi hem inline hem de block yapabiliriz.


none= 
displaye none özelliği verirseniz etiket kaybolur.
bu işlemde etiket direkt olarak silinir yer kaplamaz.
eğer etiket kaybolsun fakat bulunduğu yeri kaplasın  isterseniz:
 visibilitiy:hidden; ile yapabilirsiniz.

html etiketlerimiz varsayılan olarak inline dır.
fakat bazı etiketler inline-block veya block olabilir.
etiketlerin display özelliklerini öğrenebilmek için devTools dan user agent a bakabiliriz.
user agent= tarayıcıdan gelen değerdir.

etiketlerin display özelliklerini değiştirmek için :
 
display: ;   özelliğini kullanabilirsiniz.




                    -CSS GRİD DERS 7 ÖNEMLİ-
grid sayfayı yatay ve dikey olarak sütunlara bölerek kullanma işlemidir.
grid=ızgara demektir.

col= sütundur 
row =satır.

bizler col ve row a göre hizalama yaparız.

grid uygulaması nasıl yapılır:
gridde birden fazla elementi konumlandırmak için bir kapsayıcıya ihtiyaç duyarız.
grid işlemlerimizi kapsayıcı üzerinden yaparız.

bu kapsayıcının display özelliğinin grid olması gerekir:

    <style>
        .kapsayici{
            display: grid;
            grid-template-columns: 100px 100px;
        }
    </style>
  </head>
  <body>
    <h1>Hello</h1>

    <div class="kapsayici">
      <div style="background: red">kutu1</div>
      <div style="background: green">kutu1</div>
    </div>
  </body>

! grid-template-colums ile kapsayıcı içindeki elementlere genişlik değeri veririz.
bu özellikte kaç tane değer verirseniz satırda o kadar eleman bulunur.
örneğin yukarıda 2 tane değer verilmiş 3. eklenecek element alt satıra eklenir.

bizler bu uygulamada eğer fr yani free space kullanırsak css kendi ölçeklemesini ayarlar.
ve etiketlerimiz tarayıcı boyutuna göre şekil alır.

bizler konumlandırma yaparken px değerleri vermek yerine tarayıcı boyutuna uyumlu işlem yapmak için fr kullanırız.
çünkü tarayıcı boyutu küçüldükçe px değeri verdiğimiz element aynı kalacağından scroll çıkmasına sebep olur.

kullanırken: 2 fr verdiğimiz değer 1 fr verdiğimiz değerden daha fazla yer kaplar.


örnek olarak :
3 elementin 2 tanesine 100px değeri verdik ve sonuncu elemente 1 fr verdik
2 element 100px yer kaplar satırda kalan boşluğu da fr verdiğimiz element kaplar.


örnek uygulama
    <style>
      .kapsayici {
        display: grid;
        grid-template-columns: 1fr 2fr;
      }
    </style>
  </head>
  <body>
    <h1>Hello</h1>

    <div class="kapsayici">
      <div style="background: red">kutu1</div>
      <div style="background: green">kutu1</div>
    </div>


!column-gap = 
sütunların arasını açmak 
yani elementlerin arasını ayırmak için kullanılır.
px değeri vererek ayırma işlemi yapabiliriz.

örnek uygulama:
 
    <style>
      .kapsayici {
        display: grid;
        grid-template-columns: 1fr 1fr;
        height: 100px;
    *    column-gap: 5px;  *
      }
    </style>
  </head>
  <body>
    <h1>Hello</h1>

    <div class="kapsayici">
      <div style="background: red">kutu1</div>
      <div style="background: green">kutu1</div>
    </div>
  </body>

row-gap=
satırların arasını açmak için kullanılır.
px değerleri vererek ayırma işlemi yapabilirsiniz.

örnek uygulama:

      .kapsayici {
        display: grid;
        grid-template-columns: 0.5fr 0.5fr;
        height: 100px;
        column-gap: 5px;
        row-gap: 10px;
      }

    <div class="kapsayici">
      <div class="kutu" style="background: red">kutu1</div>
      <div class="kutu"  style="background: green">kutu2</div>
      <div class="kutu"  style="background: rgb(63, 0, 181)">kutu3</div>
      <div class="kutu"  style="background: rgb(128, 0, 117)">kutu4</div>
    </div>


! EĞER SADECE GAP KULLANIRSANIZ ROW VE COL DA AYNI PX DEĞERİNDE AYIRMA İŞLEMİ YAPILIR.

örnek uygulama:
     
      .kapsayici {
        display: grid;
        grid-template-columns: 0.5fr 0.5fr;
        height: 100px;
        gap: 28px;
      }
          <div class="kapsayici">
      <div class="kutu" style="background: red">kutu1</div>
      <div class="kutu"  style="background: green">kutu2</div>
      <div class="kutu"  style="background: rgb(63, 0, 181)">kutu3</div>
      <div class="kutu"  style="background: rgb(128, 0, 117)">kutu4</div>
    </div>

   
   

                                    -CSS FLEXBOX DERS 8 -
flexbox ile hizalama işlemlerini yaparız.
flexbox işlemlerimizi de kapsayıcımız üzerinden yaparız.
flex ile bir divin içinde birden fazla elemanı yan yana getirebiliriz.

bunun için kapsayıcı divimizin display özelliğine flex veririz.

örnek kullanım:

    <style>
        .kapsayici{
            display: flex;

        }
    </style>
</head>
<body>
    <div class="kapsayici">
        <div style="background-color: red;">kutu1</div>
        <div style="background: green;">kutu2</div>
        <div style="background: rgb(17, 0, 128);">kutu3</div>
    </div>

! flex in grid den farkı :

gridde kaç tane elemanın yan yana geleceğini tek tek belirtmemiz gerekir.
örnek grid-template-columns: 1fr 1fr ; bu işlemde bir satırda yanlız 2 element yan yana gelir.

eğer flex kullanmamız gerekmez display:flex olduğunda kaç tane eleman eklersek o kadar eleman yan yana gelir.

! gridde kullandığımız 1fr değerini flexte elementler üzerinde kullanabiliriz.
örnek:
elementlerin style özelliklerine flex:1; değerini verirsek griddeki 1fr özelliği ile aynı işlemi görür.

örnek uygulama:

    <style>
        .kapsayici{
            display: flex;

        }
    </style>
</head>
<body>
    <div class="kapsayici">
        <div style="background-color: red;
        flex: 1;">kutu1</div>
        <div style="background: green;
        flex: 1;">kutu2</div>
        <div style="background: rgb(17, 0, 128);
        flex: 1;">kutu3</div>
    </div>
 

!flex ile yan yana gelen elementlerin arasını açmak için column-gap özelliğini kullanabiliriz.

    <style>
      .kapsayici {
        display: flex;
        margin-top: 20px;
        column-gap: 10px;
      }
    </style>
  </head>
  <body>
    <div class="kapsayici">
      <div style="background-color: red; flex: 1">kutu1</div>
      <div style="background: green; flex: 1">kutu2</div>
      <div style="background: rgb(17, 0, 128); flex: 1">kutu3</div>
    </div>
    <div class="kapsayici">
      <div style="background-color: red; flex: 1">kutu1</div>
      <div style="background: green; flex: 1">kutu2</div>
      <div style="background: rgb(17, 0, 128); flex: 1">kutu3</div>
    </div>


! flex uygulamalarında elementleri konumlandırmak için farklı özellikler kullanabiliriz.

*justify-content  flex ile hizalama yapmaya yarar.
display flex olmadan justify-content özelliğini kullanamayız.


*space-between=
elementleri kapsayici div içerisinde element sayısına göre sağa sola ve ortaya yerleştirir.


örnek kullanım:

    <style>
      .kapsayici {
        display: flex;
        border: 1px solid black;
        justify-content: space-between;
      }
    </style>
  </head>
  <body>
    <div class="kapsayici">
        <div style="background: red;">kutu1</div>
        <div style="background: rgb(10, 204, 26);">kutu1</div>
        <div style="background: rgb(36, 10, 204);">kutu1</div>
    </div>

*space-around=
elementleri başa sona ortaya koyar ve sağdan soldan belirli boşluklar bırakır.


örnek kullanım:

    <style>
      .kapsayici {
        display: flex;
        border: 1px solid black;
        justify-content: space-around;
      }
    </style>
  </head>
  <body>
    <div class="kapsayici">
        <div style="background: red;">kutu1</div>
        <div style="background: rgb(10, 204, 26);">kutu1</div>
        <div style="background: rgb(36, 10, 204);">kutu1</div>
    </div>

space-around da 
elementler arasındaki uzaklıklar kendi arasında eşit
divin sağı ve solundaki boşluklar eşittir.



*space-evenly=
elementleri başta sonda ve ortada sıralar
space-aorund ile arasındaki fark:
space-evenly de elementler arası ve div içinde bulunan sağ ve sol boşlukların hepsi birbirine eşittir.


örnek kullanım:

    <style>
      .kapsayici {
        display: flex;
        border: 1px solid black;
        justify-content: space-evenly;
      }
    </style>
  </head>
  <body>
    <div class="kapsayici">
        <div style="background: red;">kutu1</div>
        <div style="background: rgb(10, 204, 26);">kutu1</div>
        <div style="background: rgb(36, 10, 204);">kutu1</div>
    </div>



!justify-content özellikleri elemanları yatay pozisyonda hizalar.
eğer bizler dikey pozisyonda konumlandırma işlemi yapmak istiyorsak:

*align-items özelliğini kullanmamız gerekir.

align-items özellikleri=
kapsayıcı divin yüksekliği arttığında içinde bulunan elementlerin yükseklikleri kapsayıcıyı doldurmak için artar.
eğer bizler elementlerin yüksekliklerinin kendi yükseklik değerinde kalmasını istiyorsak:
align-items: ; özelliğini kullanmamız gerekir.

flex-start:

flex-start özelliği ile elementleri sol üst kısımda hizalarsınız.
start diyerek de kullanabilirsiniz.

örnek kullanım:

    <style>
      .kapsayici {
        display: flex;
        border: 1px solid black;
        height: 300px;
        align-items: flex-start;
      }
    </style>
  </head>
  <body>
    <div class="kapsayici">
        <div style="background: red;">kutu1</div>
        <div style="background: rgb(10, 204, 26);">kutu1</div>
        <div style="background: rgb(36, 10, 204);">kutu1</div>
    </div>
  </body>

flex-center:
elementler kendi boyutlarında kalarak sol orta kısımda hizalanır.

örnek kullanım:

    <style>
      .kapsayici {
        display: flex;
        border: 1px solid black;
        height: 300px;
        align-items: center;
      }
    </style>
  </head>
  <body>
    <div class="kapsayici">
        <div style="background: red;">kutu1</div>
        <div style="background: rgb(10, 204, 26);">kutu1</div>
        <div style="background: rgb(36, 10, 204);">kutu1</div>
    </div>


flex-end:
elementler sol alt kısımda hizalanır.

örnek kullanım:

    <style>
      .kapsayici {
        display: flex;
        border: 1px solid black;
        height: 300px;
        align-items: flex-end;
      }
    </style>
  </head>
  <body>
    <div class="kapsayici">
        <div style="background: red;">kutu1</div>
        <div style="background: rgb(10, 204, 26);">kutu1</div>
        <div style="background: rgb(36, 10, 204);">kutu1</div>
    </div>


www.flexboxfroggy.com üzerinden alıştırmalar yapabilirsiniz.

            -CSS POSİTİON DERS 9-
css de position özelliği elementlerin bulunduğu yeri ayarlamaya yarar
default özelliği static  dir.

position ile etiketleri istediğimiz yerde konumlandırabiliriz.

position özellikleri:




-static-
varsayılan değerdir.
bu değerde diğer position özelliklerini kullanamazsınız.

-relative-

z-index=
z-index elementlerin öne çıkma değerlerini verdiğimiz özelliktir.
2 positionu relative olan değer birbiri üstüne binmişse z-index değeri büyük olan element üste çıkar.
! iki elementin z-indexi de aynı değerde ise alt satırda bulunan element üste çıkar çünkü kodlama yukarıdan aşağı olur.

örnek uygulama:

    <style>
      body {
        margin: 0;
      }
      .box {
        width: 200px;
        height: 200px;
        color: white;
        font-size: 30px;
        z-index: 1;
      }
      .box1 {
        background-color: red;
        position: relative;
      }
      .box2 {
        background-color: rgb(59, 19, 154);
        position: relative;
        top: -150px;
        z-index: 1;
      }
      .box3 {
        background-color: rgb(163, 211, 6);
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="box box1">kutu1</div>
      <div class="box box2">kutu2</div>
      <div class="box box3">Kutu3</div>
    </div>

!relative de  top left özellikleri kullanabilir ve z-index kullanabiliriz.



-absolute-
absolute elementin olduğu eksenden çıkmasını sağlar.
element hiçbir şey yokmuş gibi davranır.
element absolute olduğunda kapsayıcının sınırını artık kabul etmez tarayıcıyı kabul eder.
eğer bir kapsayıcı istiyorsak absolute olan elementin kapsayıcsına relative özelliğini vermemiz gerekir.
absolute olan element en yakın kapsayıcıdan body e kadar relative position arar yoksa body i esas alır.


örnek uygulama:
      
      .container{
        border: 5px solid black;
        width: 600px;
        position: relative;
      }
      .box2 {
        background-color: rgb(59, 19, 154);
        position: absolute;
        z-index: 4;
        top: 0;
        right: 0;
      }
    <div class="container">
      <div class="box box1">kutu1</div>
      <div class="box box2">kutu2</div>
      <div class="box box3">Kutu3</div>
    </div>


fixed
position özelliğini fixed yaparsak element olduğu yerde sabit kalır.
scroll ile ne kadar aşağı inersek inelim element orada sabit kalır.

örnek kullanım:

      header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0 20px;
        background-color: bisque;
        position: fixed ;
        top: 0;
        width: 100%;
    }
    </style>
  </head>
  <body>
    <header>
      <h2 class="logo">LOGO</h2>
      <nav>
        <div class="menu-links">
          <a href="#">Home</a>
          <a href="#">Products</a>
          <a href="#">Home</a>
          <a href="#">About</a>
          <a href="#">Content</a>
        </div>
      </nav>
    </header>





sticky:
scroll ile aşağı inerken elementin bize yapışarak bizimle beraber gelmesini sitiyorsak
position özelliği sticky olacak



            -CSS PSEUDO CLASSES DERS 10-
css tarafında bir özellik değişecek ya da bir özellik eklenecekse pseudo class ve pseudo elementler kullanılır.

-pseudo class-
pseudo classları kullanırken seçiciden sonra : koymak gerekir.

seçiçi:hover{

}

gibi


hover:
imleç elementin üstüne geldiğinde bir şetlerin değişmesini istiyorsak 

seçici:hover{
  hover durumunda eklenecek özellik
}



visited:
eğer bir link ziyaret edildiyse ziyaret edildikten sonra oluşacak css işaretlemelerini yazmamızı sağlar.

örnek uygulama:
   
    <style>
        .links a:visited{
            color: red;
        }

    </style>
</head>
<body>
    <!-- pseudo classes -->

    <div class="links">
        <a href="#">home</a>
        <a href="#">products</a>
        <a href="#">about</a>
        <a href="#">contact</a>
    </div>

burada linkler ziyaret edildiğinde renkleri kırmızı olacak


link:
linklerin default olarak hangi özelliklere sahip olmasını istiyorsak :

element:link{
  özellik
}
şeklinde yapabiliriz.

örnek uygulama:
 
    <style>
        .links a:link{
            color: red;
        }

    </style>
</head>
<body>
    <!-- pseudo classes -->

    <div class="links">
        <a href="#">home</a>
        <a href="#">products</a>
        <a href="#">about</a>
        <a href="#">contact</a>
    </div>

active:
elemente tıklanma anında oluşacak olan özelliği yazmamızı sağlar.

örnek uygulama:

    <style>
        .links a:active{
            color: red;
        }

    </style>
</head>
<body>
    <!-- pseudo classes -->

    <div class="links">
        <a href="#">home</a>
        <a href="#">products</a>
        <a href="#">about</a>
        <a href="#">contact</a>
    </div>

! eğer 2 class aynı özelliği barındırırsa alttaki class baskın gelir.


örnek uygulama

    <style>
        .links a:active{
            color: red;
        }
        /* buton gizli */
        .show-button button{   
            display: none;
        }
        /* show buton içindeki elemente hover olduğunda */
        .show-button:hover{
            color: red;
        }
        /* show buton içindeki elemente hover olduğunda buton elementi */
        .show-button:hover button{
            display: inline-block;
        }
    </style>


    <div class="show-button">
        show button
        <button>click</button>
    </div>

first-child:
bir seçicinin ilk elemanını alır.

last-child:
bir seçicinin son elemanını alır.



pseudo elements=
iki tane : olursa pseudo element olur.
tek :   olursa pseudo class olur.


first-letter:
bir elementin ilk harfini seçebilir özellik verebiliriz.

örnek olarak :

.pseudo p:last-child::first-letter{

}

burada p elementlerinin son elemanının ilk harfini seçer.

first-line= seçili elementin ilk satırını seçer.

* after ve before:

after:
 seçili elementin sonuna ekleme işlemi yapmaya yarar.
.pseudo p:last-child::after{

}

before:
seçili elementin sonuna ekleme işlemi yapmaya yarar.



:: selection=
bir elementi seçme işlemi yaptığımızda oluşacak olan işlemleri yazmaya yarar.





              - CSS SEÇİCİLER (SELECTORS) DERS 11-

*:
sayfadaki her ögeyi seçer.
sayfada varsa margin ve paddingi sıfırlamak için kullanılabilir.

        *{
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }



çocuk seçiciler için de kullanılabilir.

        .container *{
            background-color: aqua;
        }

container classının içindeki her elementi seçer.


#:
id leri seçmek için kullanılır.

id ler sadece tek bir elemente özel kullanılır. 

.:
nokta işareti classları seçmek için kullanılır.

! bizler bir elementin içindeki elementi seçebiliriz.

örnek:

li a{

}

bu seçici li etiketleri içerisindeki a etiketlerini seçer.


pseudo classları kullanabiliriz.


!  X+Y:

+ ile seçim yaptığımızda bir elementten hemen sonra gelen elementi seçer

örnek:

ul+p{

}

ul etiketinden sonra gelen her etiketi seçer.


CSS SEÇİCİLERİ İNTERNETTEN ARATARAK ÖĞRENEBİLİRSİNİZ.


                     -CSS ANİMASYON DERS 12-

CSS TRANSİTİON:
transition geçiş için kullanılan özelliktir.
örneğin bir dive hover durumunda farklı özellikler atanır.
bu özelliklere geçiş anını yönetmek için transition özelliği kullanılır.
!transition hover seçiciye değil normal seçiciye uygulanır.

transition-property: hangi atanan özellikte geçiş olacağını seçer.
transition-duration: geçiş hızını belirlediğimiz özellik

transition-timing-function:
ease : default olarak gelir.
ease-in: geçiş yavaş başlar ve hızlanır.
ease-out= geçiş hızlı başlar ve yavaşlar.
ease-in-out= değişim yavaş başlar hızlanır sonra yavaşlar.


            .box{
                width: 200px;
                height: 200px;
                background-color: red;
                transition-property: background-color ;
                transition-duration: 2s;
                transition-timing-function:ease-in ;

            }

            .box:hover{
                background-color: rgb(69, 217, 247);
            }






transition tek satırda yazılabilir:

transition:backgorund-color 2s,witdh 5s ease-in gibi

transition: all dediğimiz zaman bütün özellikler aynı geçişi alır.




CSS TRANSFORM:

rotate():
 elementi kendi etrafında döndürmek için kullanılır.

  .box{
    background-color: red;
    width: 200px;
    height: 200px;
    transform: rotate(45deg);
  }

  elementi 45 derece saat yönüne döndürür.
  eğer elementi saat yönü tersine çevirmek istiyorsanız -45 derece yani - kullanmalısınız.


skew():
elementi eğri şekilde yapmak için kullanılan elementtir.

      .box {
        background-color: red;
        width: 200px;
        height: 200px;
        transform: skew(45deg);
        border-top-right-radius: 100px;
    }

eleemnt 45 derece saat yönüne eğildi. - kullanırsak saat yönü tersine eğilir.


bu özellikleri hover da kullanabiliriz

      .box {
        background-color: red;
        width: 200px;
        height: 200px;
        border-top-right-radius: 30px;
        transition: all 2s;
    }
    .box:hover{
        transform: rotate(45deg);
        border-top-left-radius: 30px ;
    }

translate():
elementi yatay düzlemde sağa sola oynatır.

      .box {
        background-color: red;
        width: 200px;
        height: 200px;
        border-top-right-radius: 30px;
        transition: all 2s;
    }
    .box:hover{
        transform: translate(100px);
        border-top-left-radius: 30px ;
    }

transform a + değer verirsek sağ - değer verirsek sol tarafa kayar.

! translateX(): yatay düzlemde çalışır.
  translateY(): dikey düzlemde çalışır.

translateY de negatif değer yukarı pozitif değer aşağı kayma yapar.


scale():
elementi büyütür yani element öne çıkar.
1 varsayılan değerdir.

      .box {
        background-color: red;
        width: 200px;
        height: 200px;
        border-top-right-radius: 30px;
        transition: all 2s;
      }
      .box:hover {
        transform: scale(1.5);
        border-top-left-radius: 30px;
      }



CSS ANİMATİON:

animasyonda keyframes kullanılır.

keyframes:
birden fazla özellik kullanmak istiyorsak kullanılır.

öncelikle animasyonumuza isim vermemiz gerekir.

        animation-name: box;
        
daha sonra bir zaman vermemiz gerek.
  animation-duration: 5s;

  şimdi keyframes kullanacağız.

        @keyframes box{
        to{
            width: 600px;
        }
      }

keyframes den sonra animasyon ismimiz ile özellikleri veriyoruz.
bu özellikte sayfa yüklendiğinde elementimiz sağdan ve soldan genişleyerek 600px değere ulaşacak


animation-iteration-count: 
animasyonun sayfa yüklendikten sonra kaç kere çalışacağını gösteriyor.
eğer değer olarak infinite olarak verirsek sonsuza kadar animasyon çalışır.

  animation-fill-mode: forwards;
  BU ÖZELLİKTE ANİMASYON BİR KERE ÇALIŞACAK VE BİTTİĞİ YERDE DURACAK YANİ 600PX OLDUYSA 600PX DE KALACAK

 animation-delay:
 sayfa yüklendikten kaç saniye sonra animasyon çalışsın

    animation-direction: alternate-reverse;
    animasyon tersinden çalışır. yani 600px ise 600px den kendi px ine döner.

  animation-timing-function:
  animasyonların nasıl başlayıp nasıl biteceğini hız olarak ayarlayabiliriz.

bizler bütün bu özellikleri tek bir satırda kullanabiliriz.

animation: box 5s forwards 2s ease-in-out;
          ismi kaç saniye süreceği nasıl biteceği kaç sn sonra başlayacağı timing fonksiyonu




CSS KEYFRAMES:

keyframes:
birden fazla özellik kullanmak istiyorsak kullanılır

       .box{
        width: 200px;
        height: 200px;
        background-color: red;
        position: relative;
        top: 0;
        left: 0;
        animation: box 2s ease-in;
       }

       @keyframes box{
        to{
            width: 600px;
            top:200px;
            left: 200px;
        }
       }

burada keyframes özelliği ile boxımızı top ve leftte hareket ettirdik.
fakat bunu kullanmak için boxımızın positionu relative olmalıdır. aksi takdirde top ve left kullanılamaz.

burada top ve left başlangoç değerlerini keyframes içinde verebiliriz.

       @keyframes box{
        from{
            top: 0;
            left: 0;
        }
        to{
            width: 600px;
            top: 50px;
            left: 50px;
        }
       }

bizler animasyonun zamanını yüzdelik dilimlere bölüm işlem yapabiliriz.


     25%{
            top: 200px;
            left: 0;
         }
         50%{
          top: 200px;
          left: 200px;
         }
         75%{
          top: 400px;
          left: 200px;
        }
        100%{
          top: 400px;
          left: 400px;
        }




                    -CSS RESPONSİVE/MEDİAQUARİES DERS 13-
media sorguları tüm cihazlara uyumlu web geliştirme yapmamızı sağlar.

akıllı cihazların hayatımıza girmesiyle responsive tasarım önem kazandı.
responsive tasarımlar yapmak için media sorguları geliştirildi.

bizler sayfa genişliğine göre stillendirme işlemleri yaparız.

*
@media ile bizler belirli px aralıklarına uygun tasarım yapabiliriz.


    <style>
      body {
        background-color: black;
      }
      @media (max-width: 992px) {
        body {
          background-color: yellow;
        }
      }
    </style>


örneğin burada sayfa 992 px in altına indiğinde
body nin backgorund color u yellow olacaktır.

?max-witdh=
verilen px değerinin altına inildiğinde çalışacak olan css kodlarıdır.
örneğin @media(max-width: 762px) ==> 762px altına inildiğinde çalışılacak olan kodları içerir.

?min-witdh=
verilen px değerinin üstüne çıkıldığına çalışacak olan css kodlarıdır.
örneğin @media(max-width:600px){} ==>600px in üstüne çıkıldığında çalışacak olan kodlar.

*max-width ile min-width i birlikte kullanabiliriz.
örnek:
      
      @media (max-width: 600px) and (min-width: 900px) {
        body {
          background-color: red;
        }
      }

bu uygulamada css kodu 600px ile 900px arasında aktif olacaktır.

*örnek bir uygulama yapalım

      body {
        background: black;
      }
      h1 {
        display: none;
        color: white;
      }
      /* 1201px üstüne çıktığında large classı görünecek */
      @media (min-width: 1201px) {
        .large {
          display: block;
        }
      }
      /* belirtilen px ler arasında desktop classı görünecek */
      @media (min-width: 1025px) and (max-width: 1200px) {
        .desktop {
          display: block;
        }
      }
      /* belirtilen px ler arasında laptops classı görünecek */
      @media (min-width: 764px) and (max-width: 1024px) {
        .laptops {
          display: block;
        }
      }
      /* belirtilen pxler arasında tablets classı görünecek */
      @media (min-width: 481px) and (max-width: 768px) {
        .tablets {
          display: block;
        }
      }
      /* belirtilen pxler arasında mobile classı gözükecek */
      @media (min-width: 320px) and (max-width: 480px) {
        .mobile {
          display: block;
        }
      }
    </style>
  </head>
  <body>
    <h1 class="mobile">mobile</h1>
    <h1 class="tablets">tablets</h1>
    <h1 class="laptops">laptops</h1>
    <h1 class="desktop">desktop</h1>
    <h1 class="large">large</h1>
  </body>

  bu uygulamamızda belirli tarayıcı isimlerini class alan h1 ler oluşturduk.
  display:none ile ilk başta bu h1 leri kaldırdık.
  daha sonra @media belirli aygıt classlarının px aralıklarına uygun h1 leri tekrardan getirdik.
  bu sayede tablet üzerinden sayfaya göz atan kişi tablet classına sahip h1 i gördü.
  
                     -CSS EM&REM DERS 14-
EM= em değeri verilen etiketin kapsayıcısının px değerine göre işlem yapan size değeridir.

yani sizler bir paragrafın px değerine 1em dersek bu 16px e eşittir.
bizler html in px değerini değiştirebiliriz.
örneğin:
html{
  font-size=20px 
}

dedikten sonra
p{
  font-size=1em 
}

dersek aslında p etiketi font size değerine 20px demiş oluruz.

tabi bizler em değerini değiştirdikçe default değer ile çarpılarak değer vermiş oluruz.
1.5em demek 16*1.5 px demektir.

örneğin bir div in içerisindeki p elementine em ile değer verirsek
divimize verdiğimiz değere göre işlem yapar.
   
    <div class="container">
      <p class="container-p">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime corporis
        tempora ipsa inventore hic, quidem harum, repellendus voluptatum
        aspernatur placeat eum deleniti sit perspiciatis ipsam fugit ea
        repudiandae sed laudantium?
      </p>
    </div>

css:

.container{
  font-size:20px
}
.container-p{
  font-size:2em
}

bu işlemde container-p deki 2em değeri kapsayıcı olan container deki font size ın değerinin 2 ile çarpımına eşittir.

em değeri alan etiket ilk kapsayıcıdan başlayarak bakar
örneğin p elementinin font size ına 1.5em verdik.
p elementi üst kapsayıcılara bakar. üst kapsayıcılarda font size varsa ona göre işlem alır.eğer hiçbir kapsayıcıda font size yoksa hmtl etikeninin default değeri olan 16px e göree işlem alır.

BU YAPILAR RESPONSİVE YAPILARDA ÇOK İŞİMİZE YARAR.


REM=rem değeri direkt olarak html etiketinin değerine bakar 
örneğin html (<hmtl></html>) etiketinin default font-size px değeri 16px dir.
bizler eğer bir etiketin font-size değerine 1.5rem dersek:
16*1.5 =24px demiş oluruz.
bu tür değerleri rem ile vermek bizlere responsive tasarımlarda tekrardan px ayarlaması yapmadan responsive e uygun bir tasarım yapımı sunar.

bizler profesyonel çalışmalarda em ve rem değerlerini kullanırız.

tabi bu işlemlerde 16px default değerinde sürekli hesaplama yapmak zor olabilir.
bu yüzden html in default değerini 10px yaparak rem işlemlerini yapabiliriz.

kullanıcı tarayıcısında zoom yapmış olabilir.bunu yaptığında bizim etiketlerimizin tarayıcı zoomuna göre hareket etmesi için de hmtl e 62.5% değerini verirsek kullanıcı zoom yaptığında etiketlerimiz ona göre işlem alır ve boyutlama konusunda sıkıntı çekmeyiz.



            -CSS DEĞİŞKENLER DERS 15-
css değişkenleri web tasarımında sıkça kullandığımız css stil özelliklerinin yerine kullanabildiğimiz değişkenlerdir.
Değişkenler tasarımda tekrara düşmeme açısından bize kolaylık sağlar.
Tasarımda değiştirilmesi gereken öğeler tek bir yerden değiştirilir.
Tasarımın daha düzenli olmasını sağlar.

css değişkenleri:
:root{

}
içerisinde yazılır, key ve value olarak oluşturulur.
örnek:
:root{
  blue:#1e90ff;
  white:#fffff
}
blue key #1e90ff value dir.

bu değişkenleri oluşturduktan sonra buradaki değişkenleri başka stil özelliklerinde kullanmak için var() anahtar kelimesini kullanıyoruz.

örnek:
     :root {
        --blue: #1e90ff;
        --white: #ffffff;
      }
      body {
        background-color: var(--blue);
      }
var() içerisine kullanacağımız css özelliğinin key değerini alıyor.

şimdi sizlere variables kullanmanın bizlere sağladığı faydayı göstereceğim:

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  background-color: aqua;
}
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: black;
  padding: 10px 20px;
  color: white;
}

nav ul {
  list-style: none;
  display: flex;
  gap: 10px;
}
nav ul a {
  text-decoration: none;
  color: white;
}

section {
  margin: 10px 20px;
  background-color: gray;
  padding: 20px;
  border-radius: 30px;
  color: white;
}

section button {
  border: none;
  color: white;
  background-color: black;
  outline: none;
  padding: 8px 20px;
  margin-top: 10px;
  border-radius: 30px;
}


bu normal bir css dosyasıdır. şimdi bizler variables ile bu dosyayı yeniden dizayn edeceğiz.
:root {
  --primary-color: #f70776;
  --secondary-color: #c3195d;
  --bg-color: #680747;
  --base-font-family: "Poppins", sans-serif;
  --secondary-font-family: "Mochiy Pop One", sans-serif;
}
burada değişkene atadığımız değerleri var ile 
elementler üzerinde uygulayabiliriz.
mesela bir özelliği birden fazla yerde kullandık.
daha sonra bu özelliği değiştirmek istedik.
işte bu kısımda tek tek değiştirmek yerine variables üzerinden değişiklik yapmak daha kolaydır.

!!bizler variables değerlerini belirli yerlerde ezebiliriz.
örneğin sayfanın tamamında belirli bir renk kullanılmış olsun.bizler bir divde o rengi değiştirebiliriz.
örnek:

:root{
  --bg-color:black;
}

.container{
  --bg-color:blue;
  background-color:var(--bg-color);
}

burada background color a roottaki black rengini verdik.

fakat container üzerinde  --bg-color:blue; diyerek roottaki değeri ezmiş olduk.
