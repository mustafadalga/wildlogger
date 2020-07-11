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
#### Çalıştırılan hedef sistemde ,hedefin bağlantı bilgilerini,cihaz sistem bilgilerini,işletim sistemi üzerinde çalışan processler ve  çalışmayan servislerin listesini,klavye tuş kayıtlarını , kopyalama -  yapıştırma panolarını  ve ekran görüntüleri yakalayıp belirtilen email adresine, belirtilen zaman aralıklarında gönderen,Windows işletim sistemi için tasarlanmış bir keylogger. 

### Detay

<table>
 <tr>
  <td>
   :arrow_right:
  </td>
  <td>
 Log kayıtları ve ekran görüntülerini rapor olarak göndermek için 2 farklı thread kullanılmaktadır; 
 <p>:heavy_check_mark:1.thread , Belirtilen mail adresine , belirtilen süre bazında log kayıtlarını gönderir.   </p>
 <p>:heavy_check_mark: 2.thread , Belirtilen süre de bir ekran görüntüleri  alır.Eğer alınan ekran görüntüsü sayısı 10 olursa , ekran görüntülerini belirtilen  mail adresine raporlar ve hedef bilgisayarda bir anormallik saptanmaması için silinir.</p>
  </td>  
 </tr>
   <tr>
  <td>
   :arrow_right:
  </td>
   <td>
Raporlama işlemleri için varsayılan olarak google mail sunucusu kullanılmaktadır.  
  </td>  
 </tr>
 <tr>
   <td>
   :arrow_right:
  </td>
 <td>
  Eğer raporlama işlemi Gmail SMTP  sunucusu kullanılarak yapılacaksa <a href="https://www.google.com/settings/security/lesssecureapps" alt="Daha az güvenli uygulama erişimi">Daha az güvenli uygulama erişimi</a>  açık olmalıdır.
 </td>
 </tr>
  <tr>
    <td>
   :arrow_right:
  </td>
 <td>
  Wildlogger'in hedef bilgisayarda sürekli çalışmasını sağlayan <strong>persistent</strong> metodu varsayılan olarak pasif hale getirilmiştir.
 </td>
 </tr>
 <tr>
    <td>
   :arrow_right:
  </td>
 <td>
  Wildlogger, exe'ye dönüştürüldüğünde hedef bilgisayar üzerinde sürekli olarak çalışması için <strong>persistent</strong> metodunun aktif hale getirilmesi gerekir.<strong>Persistent</strong> metodu aktif edildikten sonra;  
<p>:heavy_check_mark: Çalıştırılan Wildlogger dosyası appdata klasörüne "Windows Explorer" adı ile kopyalanır,  </p>
<p>:heavy_check_mark: Kayıt defterinde,Windows'un başlangıçta çalışan uygulamalarının arasına  keylogger dosyasının  yolu eklenerek süreklilik sağlanır.</p>
 </td>
 </tr>
 </table>


### Kullanım için kurulacak modüller
* Windows için kurulum
```
python -m pip install -r .\requirements.txt
```

### Kullanım
```
python wildlogger.py 
```
