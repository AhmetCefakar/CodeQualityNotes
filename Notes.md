# Alttaki Notlar Yazılım Yaklaşımlarındaki Detay Noktaları İçermektedir

>- Yazılımda en zor şey; anlama, anlatma ve iletişimdir. Bu metimdeki notlar bu sorunların çözümlerini içermektedir



## Software Philosophy

### Programing Languages
>- Programlama dilleri, program geliştirme yaklaşımlarına göre farklı kategorilere ayrılırlar. Bu ayrım dillerin derlenme şekilleri(Compiling and Interpreting) olabilir, uygulama geliştiriciyi makine dilinden ne düzeyde soyutladığı olabilir, hangi tür kodlama yaklaşımı(Procedurel, OOP vb.) kullandığı olabilir ve Imperative-Declerative yaklaşım gibi daha birçok metrik vardır.
>- Programlama dilleri yukarada sayılan ve sayılmayan bir çok metriğin bazılarını destekler, bazılarını desteklemez, bazılarını kısmen, bazılarını hibrit yapılarla destekler.
>- Yukarıda bahsedilen yaplaşımları programlama dünyasına tam manasıyla giriş yapmadan ve tecrübe etmeden akılda kategorileştirmek ve özümsemek çok zordur!
>
------

------



## Technical Terminologies

- **MVP(Minimum Viable Product)**: En az ihtiyaçlar göz önünde bulundurulan üründür, bu mantık bir çok farklı yaklaşım ile kullanılabilir.
- **WSDL**: Web Service Decleration Language

------

------



## Technical Technologies

1. **Slack**: Şirketlerde ekipler arasında haberleşmeyi sağlayan çoklu platform(web, ios, android, desctop) desteği olan döküman paylaşım ve arama gibi gelişmiş özellikleri olan bir platform. Kurulan guruplaya davetiye mantığıyla üye olunabiliyor.
2. **Markdown**: Sadece yazı yazmaya odaklanmak için(renk-font-biçimlendirme yok) geliştirilen bir teknolojidir, içerikler '.md' uzantılı dosyalarda saklanır, github-gitlab gibi git servislerinde 'ReadMe' dosyaları bu format ile yazılıyor.
   1. **Markdown için editörler**: Typora(desktop)



------

------



## OOP(Object Oriented Programing)

### OOP Philosophy
>- Program an interface, not an implementation(Arayüzlere programlama yap, gerçekleştirmelere değil)[Gerçekleştirme: Sınıf new'lemedir] 
>-  Depend on abstructions, not on concretions(Arayüzlere bağımlı ol, gerçekleştirmelere değil)[Gerçekleştirme: Sınıf new'lemedir]

### Class-Object Informations
1. Class yapıları felsefi olarak insanların idrak ettikleri dünyayı elektronik sistemlerde anlaşılması kolay şekilde modellemek için kullandıkları yapılardır.
1. Class-Object farkı; 	
	1. Class bir şablondur ve objeler bu şablondan türetilirler.
	1. **Class** : Sadece HardDisk üzerinde(yani elektronik cihazın depolama alanında yer kaplayan) bulunan yapılardır.
	1. **Object(Nesne)** : Class'tan türetilen ve Ram üzerinde yer kaplayan yapılardır, bu nedenledir ki nesne yapıları için yaşayan yapılar denir.


### Class yazma Standartları
1. Bir Class içinde doğrudan assignment(atama) işlemi yapılmaz, eğer atama işlemi yapılacaksa sınıfın kurucusunda bu atama işlemi yapılır.
1. Bir metod'a dörtten fazla parametre geçiliyorsa bu parametreler bir model olarak paketlenmelidir(bazı istisnai durumlar dışında bu kurala uyulmalıdır).


### Behaviors(Function&Method)
01. Programlama dillerindeki yaklaşıma göre dillerdeki işlevselliklere function(fonksiyon) ya da method(metod) denir.
1. **Function(fonksiyon)** : Genellikle procedurel(C, Kısmen C++ vb.) temelli dillerde tek başına tanımlanan işlevselliklerdir.
1. **Method(Metod)** : OOP(Nesne yönelimli) temelli dillerde sınıf yapılarının içerisinde tanımlanan işlevselliklerdir.
1. **Kısaca**: Class yapılarının içinde kullanılınca 'Method' olarak isimlendirilir, bir Class yapısına bağlı olmadan kullanılınca 'Fonksiyon' olarak isimlendirilir.

### Polymorphism
1. OOP yaklaşımında Method-Class seviyesinde olan çok biçimliliktir. Polimorfizm önceden hangi metodun ya da nesnenin koşturulması gerektigi bilgisine sahip olmadan, kullanılan veri tipine(data type) ya da sınıfa(class) bağımlı metot ya da nesne seçimi yöntemidir.
	1. Method'ların 'Virtual-Overwride' olarak kullanılmaları, metod'ların çok biçimli olmalarını sağlar.
	1. 'Implementation-Inheritance' yaklaşımı 'Upcasting' kullanımı ile sınıf seviyesinde çok biçimliliğin kullanılmasını sağlar.
- **Upcasting**: Bir ata Class ya da Interface değişkenine kendini inherid(ya da implement) eden sınıfın nesnesinin atanması işlemidir.

------

------



## Software Architectures

### UML-Class Diagrams
1. **Class Diagrams**: Class'lar arası ilişkileri(ki bu ilişkiler 'Is A' ve 'Has A' olarak ikiye ayrılır) götermek için kullanılan modelleme dili.
1. **Is A Relationship(Generalization-Specialization, Inheritance-Implementation)** : Kalıtım ilişkilerini gösterir. 'Inheritance, Implementation' farklı olarak 'Generalization, Specialization' olarakta isimlendirilir.
1. **Has A Relationship(Association)**: Bir sınıfın başka bir sınıf içinde property olarak kullanılma ilişkilerini gösterir. "Has A" ilişkilerinin temelde "one-one, one-many, many-many" gibi üç adet türü vardır.
1. **Association**: Bilme, Generalization-Specialization: Kalıtım ilişkileridir.
1. Association ilişkilerin bir ileri türleri, Aggregation ve Composition ilişkileridir.



### UML-Sequence Diagrams

1. **Sequence Diagrams**: Object(nesne)'ler arası etkileşimi(interaction) modellemek için kullanılır, nesneler arası etkileşim motodlar üzerinden olur.



### Design Patterns(Tasarım Desenleri)

1. Aslında Tarasım desenleri kısaca Nesneler arasındaki ilişkileri yönetmektir ya da birden fazla nesnenin nasıl yönetileceğidir.
2. Bir tasarım deseni "Name, Problem, Solution, Result" olmak üzere dört kademeden ibaretttir.

------

------



## Software Architectures Layers

### Data Access Layer
1. Bu katmanda veri kaynaklarına erişim ile ilgili işlemler yapılır.
1. **ORM(Object Relation Mapping)**: Veritabanına erişimi sağlayan ve veritabanı tablolarının programlama tarafındaki karşılığı sınıflar ile yönetilmesini sağlayan teknolojilerdir.
	1. **Mapping**: Veritabanı tablolarının programlama tarafındaki karşılığı olan sınıfları yönetmek için kullanılan(anahtar kolonu, colon adı vb. belirlemek) yönergeler.
	1. **Context(EF)-Session(Hibernate)-vb.**: Veritabanı bağlantısının sağlanmasını sağlayan sınıflardır.
1. **Micro ORM**: İlgili teknoloji platformunda veritabanı bağlantısı sağlayan sınıfların üzerinden veritabanı işlemlerinin ORM yapılarından daha basit yaplaşımla yapan yaklaşımlardır. ORM yaklaşımından daha hızlıdır.



### Business Logic Layer

Boş

### Presentation Layer

Boş

### Service Layer

Boş

### User Interface Layer

Boş



## Software Test(TDD-TFD)

1. Mimari tasarımda "Business Layer ve UI Layer" katmanı için testlerin yapılması yeterlidir. Temel olarak yazılım testleri dört evreden oluşur, "Unit Test, Integrated Test, System Test, Application Test"
1. Unit Test: Kodu yazan kişi tarafından yapılır. Unit Tast yazabilmak için yazılımın SOLID standartlarını büyük ölçüde sağlaması gerekir.
1. Integrated Test: 
1. System Test: Yük-Performans-stres testlerinden oluşur 
1. Application Test: Klasik kullanıcı testleridir, Kabul Testi olarak'ta adlandırılır.



## ORM Technologies

1. **Lazy Loading**  : Veritabanından çekilen bir kaydın ya da kayıt listesinin ilişkili oldoğu diğer tablolardaki verilerin ilk sorguda varsayılan olarak getirilmediği durumdur, ihtiyaca göre ilişkili verilen getirilir. Bu yöntem ilişkili kayıt sayısı çoksa performans problemi oluşturur.
1. **Eager Loading**  : Veritabanından çekilen bir kaydın ya da kayıt listesinin ilişkili oldoğu diğer tablolardaki verilerin ilk sorguda belirtilenlerinin  getirildiği durumdur.
1. **Explicit Loading**: Veritabanından çekilen bir kaydın ya da kayıt listesinin ilişkili oldoğu diğer tablolardaki verilerin ilk sorgudansonra gerkli olanlarının belirtilerek ilk çekilen entity nesnesine eklendiği durumdur.

 #### Kaynaklar;
- https://www.c-sharpcorner.com/article/eager-loading-lazy-loading-and-explicit-loading-in-entity-framework/
- https://www.youtube.com/watch?v=cFJiyovYwM

------

------



## Araştır



### Security

**Cross-site scripting attacks**:

**SQL injection attacks**:

**Cross-Site Request Forgery (CSRF)**:

**Open redirect attacks**:



------

------



## Düzenle

* **SoC(Separation Of Concerns)**: SoC, yazılımdaki elemanların kendilerine özel olmasını, sorumluluklarının kendilerine ait olup, başka elemanlar ile paylaşmamasını söyler. Yazılım içindeki bileşenlerin bir birine bağlılık derecesi(coupling) ve bileşenler içerisindeki sorumluluk ilişksi(cohesion), 
  SoC prensibi için önemli iki kavramdır. Bileşenlerin bağlılık derecesinin düşük olması ve bir bileşen içindeki sorumluluk ilişkisinin yüksek olması her zaman tercih edilmelidir. Yani low-coupling, high-cohesion olmazsa olmaz!

* **AOP(Aspect Oriented Programming)**: Aspect Oriented Programming’in odak noktası ise konuların ayrımıdır (Separation of Concerns). Object Oriented Programming’de soyutlamaya (Abstraction) giderekte kodun tekrar kullanılabilirliğini, okunabilirliğini ve genişletilebilirliğini ve sınıfların birbirine sıkı sıkıya bağlı olmamasını(Loosely Coupled) olmamasını sağlayabiliriz ama bir noktaya kadar. O nokta geldiğinde ise AOP kesişen ilgilerimizi ele alarak onları tamamen bağımsız (Independent) hale getirmektedir. Bu sayede her bir kesişen ilgimiz, kendi içerisinde bağımsız olarak geliştirilebilir ve tekrar kullanılabilir hale gelmektedir.
  - AOP iki türlü uygulanabilir(Compiling diller için), 1: "IL Weaving" 2: "Method Interseption".
  - Interpreter dillerde sadece "Method Interseption" yöntemi ile AOP implement edilir.


* **CCC(Cross Cutting Concern)[Enine(Çapraz) Kesişen İlgiler]**: Yazılımların kod tabanları incelendiğinde, bazı noktaların(ilgilerin) farklı katman ve modüllerde sürekli tekrar ettiği farkedilir.Mesela exception handling, transactionlar, güvenlik kontrolleri, caching, loglama vb. gibi ilgiler(concern) yazılımların en çok tekrarlanan kısımlarından bazıları. Bu ilgiler literatürde cross-cutting concerns olarak geçmekte.

* **IOC(Inversion Of Control)**: Uygulama içerisindeki nesne yaratma sürecinin sizden alınması ve bunun bir çatıya (framework) devredilmesine Inversion of Control denir.
  * '**DI**(Dependency Injection), **IOC**(Inversion Of Control), **DI**(Dependency Inversion)' kavramları bir birleriyle bağlantılı konulardır ve SOLID prensiplerinin 'D' harfi ile ilgilidir

- **Model Driven Architecture(MDA)** : 
- **Domain Driven Design(DDD)**        :  