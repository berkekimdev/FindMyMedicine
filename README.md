# Find My Medicine (İlacımı Bul)
### Bu projeyle, hasta bireylerin ihtiyaç duydukları  ilaçlara daha rahat ulaşmalarını sağlanacaktır. Geliştirilecek sistem, özellikle ciddi hastalıklara sahip insanların, geliştirilecek sistem sayesinde ilaçlarının hangi eczanelerde bulunduğunu öğrenmelerini kolaylaştıracak ve en yakın konumdaki ilacın bulunduğu konumu belirleyecektir.
####  Backend : **Java 17**, **Spring Boot**, **Spring Web**, **Spring Security**, **Spring Data JPA**, **MySQL Driver**, **Lombok**, **Spring Boot DevTools**, **JWT (JSON Web Token)**, **Maven** 
####  Frontend : **React JS**, **Axios**, **React Router**, **Vite**, **Jest**, **ESLint**
#### Tools : **Docker**, **Kubernetes**, **Jenkins**, **Prometheus**, **Grafana**,**Helm**, **Git**  **Postman** 
#### Not : Dockerfile, Kubernetes Deployment ve Service Yaml's, Helm, Prometheus, Grafana ve Jenkins gibi sistemlerin dosyaları ve fotoğrafları için [bu linke](https://github.com/berkekimdev/DockercomposeandKubernetesYamls) tıklayabilirsiniz.

## Sistemin Çalışması ve Senaryosu
### Kullanıcının siteye girdiği andan itibaren  yapabilecekleri fotoğraflarla anlatılmıştır.  Site, toplamda üç farklı kullanıcı türünü  düşünerek tasarlanmıştır: Hasta, Eczane ve Admin.
- **Hasta** , ihtiyaç duyduğu eylemleri gerçekleştirebilecek yetkilere sahiptir. Kullanıcı girişi yapmasına gerek olmadan, yetkisi dahilinde olmayan alanlara erişimi engellenmiştir. İlaç arama gibi sistemi etkilemeyen işlemleri gerçekleştirebilir.  
- **Eczane** , sisteme kayıt olmak zorundadır ve eczane olduğunu kanıtlamadan sisteme giriş yapamaz; hesabı inaktif modda bekler. Eczane, gerekli belgeleri Admin’e e-posta ile gönderdikten sonra Admin, bu kullanıcının hesabını aktif hale getirir. Hesap aktif olduktan  sonra eczane, ilaç ekleyebilir, stok güncelleyebilir ve profil bilgilerini değiştirebilir.   
- **Admin** ise, kayıtlı eczaneleri aktif veya inaktif hale getirebilir. Ayrıca, ilaç bilgilerini değiştirebilir; bu yetki yalnızca Admin kullanıcısına aittir çünkü kötü niyetli bir eczane tüm veritabanını bozabilir. Admin, ilaç silme gibi işlemleri de yapabilir.   

- #### Sistem ilacın ismine göre, ilacın grubuna göre, ilacın etken maddesine göre sorgu yapılabilir. Sorgudan sonra ilaçların bilgileri çıkar ve anlık olarak toplam kaç adet stok bulunduğu yazar. Kullanıcı **Eczanede Bul** seçeğine tıklayarak elinde ilacın stoğu olan eczaneleri listeyebilir. Kendisine en yakın eczanenin bilgilerine ve  haritalar üzerinden konumuna erişebilir. Eczane ise sisteme inaktif olarak kayıt olabilir ve belgelerini onaylattıktan sonra giriş yapabilir. Eczane ilaç ekleyebilir, ilaç stok güncelleyebilir, ilaç bilgilerini değiştirebilir, şifresini ve bilgilerini güncelleyebilir. Kullanıcı Nönetçi eczaneleri bulabilir, kendisine en yakın eczaneleri listeyebilir, bütün ilaçları ismine göre, grubuna göre ve etken maddesine göre listeyebilir. Admin kullanıcısı bütün özellikleri kapsayarak kullanıcı aktif etme gibi özelliklere sahiptir.

![GenelSayfa1.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/GenelSayfa1.JPG)
![kayitol4.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/kayitol4.JPG)
![kayitol5.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/kayitol5.JPG)
![girişsayfasi6.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/girişsayfasi6.JPG)
![kullaniciaktifet8.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/kullaniciaktifet8.JPG)
![girişyapmışsayfa7.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/girişyapmışsayfa7.JPG)
![İlaçlar9.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/İlaçlar9.JPG)
![İlaçlar10.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/İlaçlar10.JPG)
![ilaçlar11.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/ilaçlar11.JPG)
![İlaçGrubu13.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/İlaçGrubu13.JPG)
![EnYakınEczaneler14.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/EnYakınEczaneler14.JPG)
![EczaneListele15.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/EczaneListele15.JPG)
![İlaçArama17.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/İlaçArama17.JPG)
![İlacGrubuArama18.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/İlacGrubuArama18.JPG)
![İlaçEtkenMaddeArama19.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/İlaçEtkenMaddeArama19.JPG)
![İlaçEkleme20.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/İlaçEkleme20.JPG)
![İlaçEkleme21.png](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/İlaçEkleme21.png)
![İlacStokDegistir21.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/İlacStokDegistir21.JPG)
![İlacStokDegistir22.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/İlacStokDegistir22.JPG)
![KullaniciBilgileriDegistir23.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/KullaniciBilgileriDegistir23.JPG)
![İlaçSil24.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/İlaçSil24.JPG)
![İlacBilgileriDegistir25.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/İlacBilgileriDegistir25.JPG)
![İlaçBilgileriDeğiştir26.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/İlaçBilgileriDeğiştir26.JPG)
![HarfeGöreAra29.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/HarfeGöreAra29.JPG)
![nöbetçieczaneler16.JPG](https://github.com/berkekimdev/FindMyMedicine/blob/main/images/nöbetçieczaneler16.JPG)

