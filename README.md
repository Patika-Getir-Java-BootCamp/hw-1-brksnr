[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/7TXVPuTD)


## 1 – Why we need to use OOP ? Some major OOP languages ?​ 
Object-Oriented Programming, **nesneler kullanılarak gerçekleştirilen**, işleri daha düzenli, yönetilebilir ve güvenli hale getirmek için kullanılan bir yaklaşımdır. Yapımızı OOP'nin temel prensiplerine uygun şekilde oluşturduğumuz taktirde **kodumuzu daha anlaşılabilir ve takibi kolay hale getirebiliriz.**  

### OOP’yi Kullanmanın Önemli Nedenleri  
- **Daha Anlaşılır ve Düzenli Kod:** Nesneler sayesinde kodlar daha düzenli hale gelir ve mantıklı bir şekilde sınıflara ayrılır.  
- **Tekrar Kullanılabilirlik:** Kalıtım (Inheritance) sayesinde mevcut kodları tekrar tekrar kullanabiliriz.  
- **Bakımı Kolaylaştırır:** Değişiklikler sadece ilgili sınıfta yapılır ve diğer kısımlara zarar vermeden düzenlemeler yapılabilir.  
- **Esneklik ve Genişletilebilirlik:** Çok biçimlilik (Polymorphism) sayesinde farklı nesneleri aynı arayüzle işleyebiliriz.  
- **Güvenlik:** Kapsülleme (Encapsulation) sayesinde veriler korunur ve dışarıdan müdahale edilmesi engellenir.  

## OOP PRINCIPLES  
- **Encapsulation (Kapsülleme):** Verileri ve işlevleri tek bir birimde toplamak ve dışarıya yalnızca gerekli olanları sunmak.  
- **Inheritance (Kalıtım):** Mevcut bir sınıftan yeni bir sınıf türeterek kodun tekrar kullanılabilirliğini sağlamak.  
- **Polymorphism (Çok Biçimlilik):** Aynı işlevin farklı sınıflar tarafından farklı şekillerde gerçekleştirilmesi.  
- **Abstraction (Soyutlama):** Gereksiz detayları gizleyip, yalnızca önemli kısımları ön plana çıkarmak.
  
## Some major OOP languages  
- **Java**  
- **C++**  
- **Python**  
- **C#**  
- **Ruby**  
- **Swift**  
- **Kotlin**


## 2 - Interface vs Abstract Class?

Interface Nedir?
Interface, bir sınıfın yapması gereken ama nasıl yapacağına dair bir şey belirtmeyen bir sözleşmedir. Yani, bir interface tanımladığınızda, o interface’i implement eden sınıfların o interface’deki metotları uygulamak zorunda olduğunu söylersiniz. Interface'ler sadece metot imzaları (signature) ve sabitler (constants) içerir, ama herhangi bir metot gövdesi barındırmaz.

Abstract Class Nedir?
- Abstract class, tam olarak tamamlanmamış bir sınıftır. Yani, abstract sınıflarda hem tamamlanmış metotlar (gövde içeren) hem de tamamlanmamış metotlar (soyut metotlar) bulunabilir. Abstract class, ortak özellik ve davranışları alt sınıflara miras bırakmak için kullanılır. Bu sınıfı doğrudan nesne oluşturmak için kullanamayız, ancak alt sınıflar bu sınıfı genişleterek kullanılabilir.

Interface ve Abstract Class Arasındaki Farklar
- Metot İçeriği: Interface’ler sadece metot imzaları içerirken, abstract class'lar hem tamamlanmış hem de soyut metotlar içerebilir.
- Birden Fazla Miras Alma: Java'da bir sınıf birden fazla interface’i implement edebilir, ama sadece bir abstract class’tan extend edebilir. Yani, interface’ler çoklu kalıtım desteklerken, abstract class’lar sadece tekil kalıtım destekler.
- Fields (Alanlar): Interface’lerde genellikle sabitler (constants) bulunur, ancak abstract class'larda hem değişkenler hem de sabitler olabilir.
Constructor: Abstract class'lar constructor içerebilirken, interface’ler constructor içeremez.

Özetle
Interface: Bir sınıfın hangi metotları implement etmesi gerektiğini belirtir, fakat nasıl yapılacağını tanımlamaz.
Abstract Class: Hem soyut hem de somut metotlar içerebilir ve alt sınıflar için temel davranışlar sağlar.


## 3 - Why We Need equals and hashCode? When to Override?

equals ve hashCode Nedir?
equals metodu, iki nesnenin eşit olup olmadığını kontrol etmek için kullanılır. Java’daki varsayılan equals metodu, nesnelerin bellek adreslerine bakarak karşılaştırma yapar. Ancak, genellikle nesnelerin içeriklerini karşılaştırmak istenir. Bu nedenle, çoğu zaman equals metodunu özelleştirmek gerekebilir.

hashCode metodu ise, bir nesneyi hash tablosuna yerleştirebilmek için kullanılan bir değeri döndürür. Bu değer, nesnenin bellekteki yerini hızlıca bulmamıza yardımcı olur. hashCode metodunun doğru çalışabilmesi için, eşit kabul edilen iki nesnenin hash kodlarının da aynı olması gerekir.

Neden İhtiyacımız Var?
- equals metodu, nesnelerin içeriği açısından karşılaştırılmasını sağlar. Eğer iki nesne aynı veriye sahip oluyorsa, equals metodu doğru şekilde implement edilmemişse, bu iki nesne birbirinden farklı kabul edilebilir ve yanlış sonuçlar alınabilir.

- hashCode metodu, nesnelerin hash tablosunda düzgün şekilde yerleştirilmesini sağlar. Eğer equals metodu eşit olan nesneleri doğru bir şekilde kontrol etmiyorsa, hashCode metodu da hatalı çalışabilir ve bu da veri yapılarının doğru çalışmamasına neden olabilir. - - - - Özellikle HashMap ve HashSet gibi koleksiyonlarda, eşit nesnelerin aynı yeri paylaşması gerektiği için hashCode metodunun doğru implementasyonu önemlidir.

Ne Zaman override Edilmeli?
- Eğer bir nesne, içerik bazlı karşılaştırma yapmanız gereken bir durumda kullanılacaksa, yani equals metodunu düzgün çalıştırmanız gerekiyorsa, o zaman equals metodunu override etmelisiniz.

- hashCode metodu da genellikle equals metodu ile paralel olarak override edilmelidir. Yani, iki nesne eşitse, onların hash kodlarının da eşit olması gerekir. Bu kuralı sağlamak için, equals metodunu override ettiğinizde hashCode metodunu da override etmelisiniz.

- Örneğin, HashSet gibi koleksiyonlarda nesnelerin eşit olup olmadığını kontrol etmek ve bunları saklamak için equals ve hashCode metodları düzgün şekilde çalışmalıdır. Eğer her ikisi de doğru bir şekilde override edilmezse, koleksiyonlar düzgün çalışmayabilir.

Özetle, eğer nesnelerin eşitliklerini içeriklerine göre kontrol etmek istiyorsanız ve bu nesneleri koleksiyonlar gibi veri yapılarında kullanacaksanız, equals ve hashCode metodlarını override etmek gereklidir.


## 4 - Diamond Problem in Java? How to Fix It?

Diamond Problemi Nedir?
Java, sınıflarda çoklu kalıtımı desteklemez; yani bir sınıf sadece tek bir sınıftan miras alabilir. Ancak interface'ler konusunda bu kısıtlama yoktur. Bir sınıf birden fazla interface'i implemente edebilir. Fakat bu interface'lerin bazı ortak metotları varsa, hangi metodun uygulanacağı konusunda belirsizlik yaşanır. Bu durum, programın beklenmedik şekilde çalışmasına veya hatalı sonuçlar üretmesine neden olabilir.

Diyelim ki bir sınıf, iki farklı kaynaktan aynı özelliği veya davranışı miras almak istiyor. Bu durumda, hangi üst sınıfın ya da interface'in o özelliğini kullanacağı konusunda kararsızlık ortaya çıkar. İşte bu kararsızlık "diamond problem" olarak adlandırılır. Örneğin, iki farklı interface aynı metodu tanımladığında, bu interface'leri implemente eden bir sınıf, hangi metodun geçerli olduğuna karar vermekte zorlanabilir.

Diamond problem, çoğunlukla interface'ler arasında ortaya çıkan, aynı metotların farklı kaynaklardan gelmesiyle oluşan bir belirsizliktir. Java'da bu problemi çözmek için default metotları kullanarak veya super anahtar kelimesi ile hangi metodun tercih edileceğini belirterek tasarımınızı yapmanız gerekir. Bu şekilde, uygulamanızın tutarlı ve beklediğiniz şekilde çalışmasını sağlayabilirsiniz.

Bu Problemi Nasıl Çözebiliriz?

Default Metotları Kullanmak:
- Java 8 ile birlikte interface'lere default metotlar eklenmiştir. Bu, interface'lerin kendilerine ait bir metodun gövdesini tanımlamasına olanak tanır. Eğer iki interface aynı default metodu sağlıyorsa, onu implemente eden sınıf bu metodu override ederek hangi davranışı kullanacağını belirleyebilir.

Super Anahtar Kelimesi ile Belirtmek:
- Eğer birden fazla interface aynı metodu tanımlıyorsa, implemente eden sınıf hangi interface'in metodunun kullanılacağını InterfaceName.super.metodAdi() şeklinde belirterek karışıklığı giderebilir. Bu yöntem, hangi metodun çağrılacağını açıkça ifade etmenizi sağlar.


## 5 - Why we need Garbagge Collector ? How does it run ?
Garbage Collector, Java gibi dillerde bellek yönetimini otomatik hale getiren bir sistemdir. Programınızda oluşturduğunuz nesneler, işlerini bitirdikten sonra bellekten temizlenmezse, bellek dolabilir ve programınız yavaşlayabilir ya da hata verebilir. İşte Garbage Collector, artık kullanılmayan nesneleri tespit edip temizleyerek bellek alanını geri kazandırır.

Garbage Collector Nasıl Çalışır?

Garbage Collector, arka planda çalışan bir süreçtir. JVM, programınız çalışırken bellek kullanımını sürekli izler. Eğer bir nesneye artık referans kalmamışsa, yani o nesneye ulaşmanın bir yolu yoksa, Garbage Collector o nesnenin artık kullanılmadığını anlar. Çalışma prensibi genellikle "işaretle ve süpür" (mark-and-sweep) algoritması etrafında döner:

- İşaretleme (Mark): Kullanılmayan, yani erişilemeyen nesneler belirlenir.
- Süpürme (Sweep): Belirlenen bu nesneler bellekten temizlenir.

Bazen, bellek içinde oluşan boşlukları daha verimli kullanabilmek için bellek sıkıştırma (compaction) işlemi de yapılır. Böylece, bellek daha düzenli hale getirilir ve yeni nesneler için yeterli alan sağlanır. Bu otomatik temizlik sayesinde, programcıların manuel olarak bellek yönetimi ile uğraşmasına gerek kalmaz ve uygulama daha stabil çalışır.

## 6 - Java 'static' Keyword Usage
Java'da static kelimesi, sınıfın kendisine ait olan elemanları tanımlamak için kullanılır. Yani, bir sınıfın örneği oluşturulmadan bu static elemanlara erişebilirsiniz. Bu durum, özellikle ortak kullanılan veriler ve metodlar için oldukça kullanışlıdır.

Örneğin:

- Static değişkenler: Tüm nesneler için ortak olan verileri tutar. Sınıfın tüm örnekleri, static bir değişkeni paylaşır.
- Static metodlar: Nesneye bağlı olmayan, direkt sınıf üzerinden çağrılan metotlardır. Bu metotlar, sınıf seviyesinde işlemler yapar.
- Static bloklar: Sınıf yüklendiği anda çalıştırılan kod bloklarıdır ve genellikle static değişkenlerin ilk değerlerinin atandığı yerlerde kullanılır.
- Özetle, static kullanım sayesinde ortak ve paylaşılabilir kaynakları yönetmek, programın daha az bellek tüketmesini sağlamak ve belirli işlemleri sınıf seviyesinde gerçekleştirmek mümkün olur.

## 7 – Immutability means ? Where, How and Why to use it ?

Immutability, bir nesnenin oluşturulduktan sonra değiştirilemez olması anlamına gelir. Yani, bir nesne yaratıldıktan sonra içeriği sabit kalır; o nesnenin herhangi bir özelliğini değiştirmek mümkün değildir.

Nerede Kullanılır?

- Değer Nesneleri: Sayılar, metinler, tarih gibi verilerin değişmeyeceği durumlarda kullanılır.
Thread-Safe Ortamlar: Çoklu iş parçacığının (thread) aynı veriye eriştiği durumlarda, immutable nesneler sayesinde veri bütünlüğü sağlanır.
Karmaşık Uygulamalarda: Özellikle büyük sistemlerde, yan etkileri azaltmak için immutable nesneler tercih edilir.
Nasıl Kullanılır?

- Final Değişkenler: Sınıf içindeki değişkenleri final olarak tanımlayarak, bu değişkenlerin sadece bir kez atanmasını sağlarsınız.
Setter Metodları Kullanılmamalı: Sınıfın özelliklerini değiştirecek metodlar eklenmez, böylece nesne oluşturulduktan sonra hiçbir değişiklik yapılamaz.
Constructor’da Atama: Tüm değerler, nesne oluşturulurken constructor aracılığıyla atanır ve sonrasında değiştirilemez.
Mutable Nesneleri Kopyalamak: Eğer immutable bir nesne içerisinde mutable bir veri varsa, o veriyi kopyalayarak dışarıya sunmak gereklidir. Böylece, orijinal nesne etkilenmemiş olur.
Niye Kullanılır?

- Güvenlik ve Bütünlük: Immutable nesneler sayesinde, nesne durumunun beklenmedik şekilde değişmesi engellenir. Bu, veri bütünlüğü ve uygulama güvenliği açısından önemlidir.
Thread-Safety: Değiştirilemez yapıda oldukları için, birden fazla thread tarafından aynı anda kullanıldıklarında sorun oluşturmazlar.
Basitlik: Değişiklik yapılmadığı için, nesnelerin durumunu izlemek ve hata ayıklamak daha kolay hale gelir.
Performans: Bazı durumlarda, immutable nesnelerin hashCode gibi değerleri cache’lenebilir, böylece performans artışı sağlanabilir.

Özetle, immutability, nesnelerin oluşturulduktan sonra sabit kalmasını sağlayarak, kodun güvenli, basit ve thread-safe olmasına katkıda bulunur. Bu yaklaşım, özellikle karmaşık ve çoklu iş parçacıklı uygulamalarda hataları azaltmak ve yönetimi kolaylaştırmak için oldukça faydalıdır.

## 8 - Composition and Aggregation means and differences ?

Composition Nedir?
Composition, bir nesnenin başka nesnelerden oluştuğu, yani parçaların bütünü oluşturduğu durumdur. Bu ilişkide, parçalar bütüne sıkı sıkıya bağlıdır. Örneğin, bir araba düşünün; motor, tekerlek gibi parçalar arabayı oluşturur. Eğer araba yok olursa, bu parçaların da işlevselliği ortadan kalkar çünkü onlar arabaya ait olup, onun yaşam döngüsüne bağlıdır.

Aggregation Nedir?
Aggregation ise, nesneler arasında daha gevşek bir ilişkiyi ifade eder. Bu ilişki, “sahiplik” (has-a relationship) anlamına gelir ama bileşenler bütünden bağımsız olarak varlıklarını sürdürebilir. Mesela, bir sınıf ile öğrenciler arasındaki ilişkiyi ele alalım. Sınıf, öğrencileri içerir; fakat sınıf kapandığında öğrenciler varlıklarını kaybetmez. Öğrenciler bağımsız varlıklar olarak başka sınıflarda da bulunabilirler.

Composition ve Aggregation Arasındaki Farklar
Bağımlılık Derecesi:

- Composition: Parçalar, bütüne sıkı bir şekilde bağlıdır. Bütün nesne ortadan kalktığında, içindeki parçalar da ortadan kalkar.
- Aggregation: Parçalar, bütünden bağımsız olarak var olabilir. Bütün nesne ortadan kalksa bile, içindeki parçalar başka yerlerde kullanılabilir.
Yaşam Döngüsü:

- Composition: İçerilen nesnelerin yaşam döngüsü, onları içeren nesne ile aynıdır.
- Aggregation: İçerilen nesnelerin yaşam döngüsü, onları içeren nesneden bağımsızdır.

Sahiplik:

- Composition: Sahiplik daha kuvvetlidir. İçerilen nesne, yalnızca o bütün için anlamlıdır.
- Aggregation: Sahiplik daha zayıftır. İçerilen nesne, başka ilişkilerde de yer alabilir.

Özetle, composition ile aggregation arasındaki temel fark, nesneler arasındaki bağımlılık derecesi ve yaşam döngüsü yönetimidir. Composition, daha sıkı ve bütünle birlikte yaşam sürecini paylaşan nesneleri ifade ederken, aggregation ise daha gevşek ve bağımsız varlıkları içeren bir ilişki türüdür.

## 9 - Cohesion and Coupling means and differences ?

Cohesion Nedir?
Cohesion, bir modül ya da sınıf içindeki elemanların birbirleriyle ne kadar uyumlu çalıştığını ifade eder. Yani, bir yapının kendi içindeki parçalarının birbirine odaklanmış ve belirli bir işi gerçekleştirmek için birlikte çalışmasını gösterir. Yüksek cohesion, bir bileşenin sorumluluklarının net bir şekilde ayrıldığını ve ilgili işlevleri bir arada topladığını anlatır.

Coupling Nedir?
Coupling, farklı modüller ya da sınıflar arasındaki bağımlılık derecesini ifade eder. Bir sistemdeki bileşenlerin birbirine ne kadar bağlı olduğu, Coupling ile belirlenir. Düşük coupling, modüllerin birbirlerinden bağımsız çalışabildiğini, değişikliklerin bir modülde diğerlerini minimum etkileyeceğini gösterir. Yüksek coupling ise bir modülde yapılan değişikliklerin diğer modülleri de etkileme olasılığını artırır.

Cohesion ve Coupling Arasındaki Farklar

Odak ve Amaç:

- Cohesion: Bir bileşenin içindeki parçaların ortak bir amacı veya işlevi paylaşmasıdır. Yüksek cohesion, yapının kendine has ve net bir sorumluluğu olduğunu gösterir.
- Coupling: Farklı bileşenler arasındaki bağlantının ne kadar kuvvetli olduğunu belirtir. Düşük coupling, modüllerin birbirinden bağımsız çalışabilmesini sağlar.
Bağımsızlık:

- Cohesion: Bir modül içindeki elemanların kendi aralarında birbirine ne kadar bağlı olduğu ile ilgilidir.
- Coupling: Farklı modüllerin birbirine olan bağımlılığıdır. Modüllerin birbirine sıkı sıkıya bağlı olmaması, sistemin esnekliğini ve sürdürülebilirliğini artırır.
Değişikliklerin Etkisi:

- Cohesion: Yüksek cohesion, bir bileşenin değişikliklerinin o bileşenin işlevselliğini bozmadan yapılabilmesini sağlar.
- Coupling: Düşük coupling, bir bileşende yapılan değişikliklerin diğer bileşenleri minimum derecede etkilemesini sağlar.

Özetle, cohesion bir modülün içindeki elemanların ne kadar uyumlu çalıştığını gösterirken, coupling modüller arasındaki bağımlılık derecesini ifade eder. İdeal bir sistem, yüksek cohesion (bir modül içindeki işlevlerin net ve odaklanmış olması) ve düşük coupling (modüller arasında zayıf bağımlılıklar) özelliklerine sahip olmalıdır. Bu şekilde, sistem daha anlaşılır, bakımı kolay ve esnek hale gelir.

## 10 - Heap and Stack means and differences ?

Heap Nedir?
Heap, programın dinamik bellek alanıdır. Program çalışırken, nesneler veya veri yapılarını dinamik olarak oluşturmak için kullanılır. Bu bellek alanında oluşturulan nesneler, programın herhangi bir yerinden erişilebilir ve genellikle Garbage Collector tarafından yönetilir. Heap'te depolanan veriler, bellek üzerinde rastgele yerleştirilir ve yaşam süreleri programın ihtiyaçlarına göre belirlenir.

Stack Nedir?
Stack, metod çağrıları ve yerel değişkenler için kullanılan bellek alanıdır. Her metod çağrıldığında, o metoda ait bir stack frame oluşturulur ve metod sona erdiğinde bu frame bellekten kaldırılır. Stack, LIFO (Last In First Out) yapısıyla çalışır; yani son eklenen eleman ilk çıkar. Bu yapı, metodların hızlı bir şekilde çağrılmasını ve geri dönülmesini sağlar.

Heap ve Stack Arasındaki Farklar

Bellek Yönetimi:
- Heap: Dinamik bellek yönetimi söz konusudur. Nesneler ve veri yapıları ihtiyaç duyulduğunda oluşturulur ve Garbage Collector tarafından temizlenir.

- Stack: Statik ve otomatik bellek yönetimi vardır. Yerel değişkenler ve metod çağrıları için kullanılır; metod tamamlandığında otomatik olarak temizlenir.

Yaşam Süresi:

- Heap: Nesnelerin yaşam süresi, onlara olan referanslar devam ettiği sürece sürer. Bu nedenle, bellek yönetimi daha karmaşıktır.

- Stack: Değişkenlerin yaşam süresi metodun çağrıldığı süre ile sınırlıdır. Metod tamamlandığında stack'teki veriler kaybolur.

Erişim Hızı:

- Heap: Rastgele erişim sağlanır fakat genellikle stack'e göre daha yavaştır çünkü bellek üzerinde dağınık yerleşir.

- Stack: Bellek, ardışık bloklardan oluştuğu için erişim oldukça hızlıdır.

Kullanım Alanları:

- Heap: Nesne oluşturma, dinamik bellek tahsisi gerektiren işlemler için kullanılır.

- Stack: Metod çağrıları, yerel değişkenler ve işlem sırasının yönetimi için kullanılır.

Özetle, heap dinamik ve daha esnek bir bellek yönetimi sağlarken, stack hızlı ve otomatik temizlenen bir yapı sunar. Her ikisinin farklı kullanım amaçları ve yönetim şekilleri vardır; bu da programların verimli ve hatasız çalışmasını destekler.

## 11 – Exception means ? Type of Exceptions ?

Exception Nedir?
Exception, programın çalışması sırasında beklenmedik bir durumla karşılaşıldığında ortaya çıkan ve programın normal akışını kesintiye uğratan durumdur. Kısacası, bir hatayla karşılaşıldığında programın ne yapması gerektiğini belirleyen, kontrol altına alınabilen olaylardır.

Exception Türleri
Exception’lar genel olarak iki ana gruba ayrılır:

Checked Exception

-  Derleme zamanında kontrol edilen ve mutlaka yakalanması veya bildirilmesi gereken hatalardır.
Örnekler:
- IOException (dosya okuma/yazma işlemleri sırasında oluşan hatalar)
- SQLException (veritabanı işlemleri sırasında oluşan hatalar)

Unchecked Exception
 
-  Çalışma zamanında ortaya çıkan ve genellikle programcının kontrolünden çıkan hatalardır. Bunları yakalamak isteğe bağlıdır, ancak hata ayıklamayı kolaylaştırır.
Örnekler:
- NullPointerException (null bir referans üzerinden işlem yapılmaya çalışıldığında)
- ArrayIndexOutOfBoundsException (dizinin sınırlarının dışına erişim yapıldığında)
- ArithmeticException (sıfıra bölme gibi matematiksel hatalarda)
Bu şekilde, exception’lar programınızın hatalı durumları kontrol altına almasını sağlar; her iki türün de kullanım amacı, hataların uygun şekilde ele alınarak programın çökmesini önlemektir.


## 12 – How to summarize ‘clean code’ as short as possible ?

- Temiz kod; basit, okunabilir ve bakımı kolay koddur.


## 13 - What is the method of hiding in Java ?

Java'da "method hiding", nesne yönelimli programlamada overriding (geçersiz kılma) kavramına benzer görünse de aslında farklı çalışan bir özelliktir. Burada kilit nokta, statik (static) metotlar ile ilgilidir. Yani, eğer bir alt sınıfta, üst sınıfta tanımlanmış olan static metotla aynı imzaya (aynı isim ve parametreler) sahip bir metot tanımlarsanız, bu metot "hiding" yani gizleme durumuna girer.

Nasıl Çalışır?

- Statik Metotlar ve Bağlama: Statik metotlar, nesne örneği üzerinden değil, sınıf üzerinden çağrılır. Bu yüzden, hangi metot çağrılacaksa, çalıştırma zamanındaki nesne türüne bakılmaz; referansın hangi sınıfa ait olduğuna bakılır.

- Alt Sınıfın Metodu Gizler: Eğer bir alt sınıfta aynı imzaya sahip bir static metot tanımlarsanız, bu metot üst sınıftaki static metodu "gizler". Ancak burada overriding (yani dinamik bağlama) gerçekleşmez; çünkü static metotlar dinamik olarak bağlanmaz.

- Çağırma Esnasında: Üst sınıf türünde bir referans kullanılarak metot çağrıldığında, referansın tanımlı olduğu sınıfa ait static metot çalışır. Örneğin, üst sınıf referansı alt sınıf nesnesine işaret ediyor olsa bile, metot çağrısında üst sınıfın static metodu kullanılır.

Kısaca özetlemek gerekirse, Java'da method hiding, alt sınıfta tanımlanan static metotların üst sınıftaki aynı imzalı static metotları "gizlemesi" durumudur. Bu durum, dinamik bağlamadan ziyade statik (compile-time) bağlama ile ilgilidir. Bu nedenle, nesne örneği hangi sınıfa ait olursa olsun, static metot çağrıları referansın türüne bağlı olarak belirlenir.

## 14 - What is the difference between abstraction and polymorphism in Java ?

Abstraction Nedir?
Abstraction (soyutlama), bir nesnenin ya da sınıfın özel detaylarını gizleyip, sadece önemli ve genel bilgileri dışarıya sunma işlemidir. Java'da bu, abstract class veya interface kullanılarak yapılır. Amacı, karmaşıklığı gizleyip, sadece kullanıcının etkileşimde bulunması gereken özellikleri sunmaktır. Soyutlama, ne yapılacağı hakkında bilgi verir, ancak nasıl yapılacağı ile ilgilenmez.

Polymorphism Nedir?
Polymorphism (çok biçimlilik), bir nesnenin birden fazla şekil alabilme yeteneğidir. Java’da polymorphism, bir metodun ya da bir nesnenin farklı sınıflarda farklı şekillerde davranabilmesini sağlar. En yaygın iki türü method overriding (metod geçersiz kılma) ve method overloading (metod aşırı yükleme)’dir. Polymorphism sayesinde aynı isimdeki bir metod, farklı nesnelerle farklı şekilde çalışabilir.

Abstraction ve Polymorphism Arasındaki Farklar
Amaç:

-  Abstraction: Detayları gizleyip sadece önemli olan bilgiyi sunmayı amaçlar.
-  Polymorphism: Aynı işlevin farklı şekillerde yapılabilmesini sağlar.
Nasıl Çalışır?

-  Abstraction: Sadece soyutlama yapılmış metodlar ve özellikler sunulur, implementasyon gizlenir.
-  Polymorphism: Aynı metodu farklı şekillerde çağırabilirsiniz, çünkü farklı sınıflarda farklı implementasyonlar olabilir.
Kullanım Alanı:

-  Abstraction: Sınıflar ve metodlar üzerinden yapılır. Kullanıcıya, sadece gerekli bilgileri verir.
-  Polymorphism: Nesneler ve metodlar üzerinden farklı davranışlar elde edilir.
Özetle, abstraction, detayları gizleyip daha genel bir bakış açısı sunarken, polymorphism farklı nesnelerin aynı metodu farklı şekillerde çalıştırmasına olanak tanır.

