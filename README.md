# MongoDb Kurulumu, LinQ ile Sorgulama ve Robomongo

####Nedir?
**MongoDb** belge tabanlı bir veritabanıdır. Esnek ve ölçeklenebilir olması başlıca tercih sebeplerindendir. Bir çok NoSql benchmark sitesinde en önde olduğunu araştırıp görebilirsiniz. Ssd disk üzerinde çalışırken büyük veri işlemlerinde yüksek performans sağlamaktadır. Büyükveri(bigdata) projelerinde **Sharding** yapısı kendisini bir adım öne çıkaran bir özelliğidir.

####Kurulum
Kurulum için [mongodb](https://www.mongodb.com/download-center#community)'nin kendi sitesinden indireceğimiz kurulum dosyası ile başlıyoruz. Biz windows için Community Server başlığı altından with ssl veya without ssl seçeneğini seçebilirsiniz. Mongodb "27017" portunda çalışmaktadır.

Kurulum tamamlandıktan sonra bir komut istemi penceresi açıp mongodb'nin kurulu olduğu yola gidip mongod.exe ile çalıştırıp mongo.exe ile mongodb'ye bağlanmış oluyoruz. Mongodb'yi bir Windows servisi olarak çalıştıtmak için bu [linkten](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/#configure-a-windows-service-for-mongodb-community-edition) yardım alabilirsiniz.

####Robomongo
Robomongo mongodb için bir arayüz aracı. Kendi [sitesinden](https://robomongo.org/download) indirebiliriz. Kurduktan sonra açtığınızda connections penceresi açılıyor. Create diyerek oluşturacağınız bağlantı ayarları mongodb'nin o bilgisayarda kurulu olduğunu varsayarak ayarlanmış olan ayarlardır. 

####MongoDb ve LinQ
Linq ile sorgulama yapabilmek diğer mongodb sorgulama özelliklerine göre yazımı kolay olandır. Tabi burada alışkanlıklara göre değişkenlik gösterebilir bir konudan bahsediyoruz :) 

VisualStudio içinde bir console app başlatıp Nuget üzerinden **mongocsharpdriver**'ı aratıp kuruyoruz. Bağımlılıkları olan MongoDb: Driver, DriverCore, BSON ve Driver.Legacy kütüphaneleri de kurulacaktır. Kurulum bittikten sonra deneme yapabiliriz. 

![](/content/images/2017/08/mongo2-1.png)
![](/content/images/2017/08/mongo1.png)

Kayıt ettiğimiz verileri linq ile çekelim şimdi.
![alt](/content/images/2017/08/mongo4.png)

Linq ile groupby gibi kodları çalıştırmak için AsQueryable yerine Aggregate metodunu kullanabilirsiniz. 

Ayrıca github'ta bulunan [MongoRepository](https://github.com/RobThree/MongoRepository) adında bir çalışma mevcut. Bu uygulamayı nugetten çekip basit ve hızlı bir şekilde mongodb üzerinde çalışacak projenize hızlı bir giriş yapabilirsiniz.

İyi çalışmalar.





