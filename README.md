```

 __          ___ _     _    _
 \ \        / (_) |   | |  | |
  \ \  /\  / / _| | __| |  | |     ___   __ _  __ _  ___ _ __
   \ \/  \/ / | | |/ _` |  | |    / _ \ / _` |/ _` |/ _ \ '__|
    \  /\  /  | | | (_| |  | |___| (_) | (_| | (_| |  __/ |
     \/  \/   |_|_|\__,_|  |______\___/ \__, |\__, |\___|_|
                                         __/ | __/ |
                                        |___/ |___/

```

### Açıklama
#### Çalıştırılan hedef sistemde ,hedefin bağlantı bilgilerini,cihaz sistem bilgilerini,işletim sistemi üzerinde çalışan processler ve  çalışmayan servisler listelerini,klavye tuş kayıtlarını , kopyalama -  yapıştırma panolarını  ve ekran görüntüleri yakalayıp belirtilen email adresine, belirtilen zaman aralıklarında gönderen,Windows işletim sistemi için tasarlanmış bir keylogger. 

*****

:arrow_right: Log kayıtları ve ekran görüntülerini rapor olarak göndermek için 2 farklı thread kullanılmaktadır;  
&nbsp; &nbsp; &nbsp; :heavy_check_mark: 1.thread , Belirtilen mail adresine , belirtilen süre bazında log kayıtlarını gönderir.  
&nbsp; &nbsp; &nbsp; :heavy_check_mark: 2.thread , Belirtilen süre de bir ekran görüntüleri  alır.Eğer ekran görüntü sayısı 10 olursa , ekran görüntülerini &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;belirtilen  mail adresine raporlar ve hedef bilgisayarda bir anormallik saptanmaması için silinir.  

:arrow_right: Raporlama işlemleri için , varsayılan olarak google mail sunucusu kullanılmaktadır.  

:arrow_right: Eğer raporlama işlemi Gmail SMTP  sunucusu kullanılarak yapılacaksa [Daha az güvenli uygulama erişimi](https://www.google.com/settings/security/lesssecureapps) açık olmalıdır.


:arrow_right: Wildlogger'in hedef bilgisayarda sürekli çalışmasını sağlayan **persistent** metodu varsayılan olarak pasif hale getirilmiştir.  

:arrow_right: Wildlogger, exe'ye dönüştürüldüğünde hedef bilgisayar üzerinde sürekli olarak çalışması için **persistent** metodunun &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;aktif hale getirilmesi gerekir.**Persistent** metodu aktif edildikten sonra;  
&nbsp; &nbsp; &nbsp; :heavy_check_mark: Çalıştırılan Wildlogger dosyası appdata klasörüne "Windows Explorer" adı ile kopyalanır,  
&nbsp; &nbsp; &nbsp; :heavy_check_mark: Kayıt defterinde,Windows'un başlangıçta çalışan uygulamalarının arasına  keylogger dosyasının  yolu eklenerek &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp; &nbsp; &nbsp; süreklilik sağlanır.



### Kullanım için kurulacak modüller
* Windows için kurulum
```
python -m pip install -r .\requirements.txt
```

### Kullanım
```
python wildlogger.py 
```
