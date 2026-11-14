# Bar Downloader – Gizlilik bildirimi / Privacy notice

[Türkçe](#türkçe) · [English](#english)

## Türkçe

Son güncelleme: 11 Kasım 2026 (sürüm 0.0.9)

Bar Downloader hesap istemez ve reklam göstermez. Kullanım verisi, analiz ya da çökme raporu toplamaz. Eklentinin gönderdiği bilgiler yalnızca bu bilgisayardaki Bar Downloader uygulamasına gider. Bizim bir sunucumuz yok.

### Eklenti neyi, nereye gönderir?

Bir indirmeyi Bar Downloader'a verdiğinizde eklenti şu bilgileri yalnızca `http://127.0.0.1:27117` adresine gönderir. Bu adres bilgisayarınızdaki uygulamadır:

- dosyanın adresi (URL) ve dosya adı,
- bağlantının bulunduğu sayfanın adresi (Referer),
- tarayıcınızın kimlik metni (User-Agent),
- yalnızca o adres için tarayıcıdaki çerezler. Böylece oturum açmanızı gerektiren dosyalar da iner.

YouTube adreslerinde yalnızca youtube.com çerezleri gönderilir. Uygulama bunları ancak siz onay verirseniz kullanır. Eklenti bu bilgileri başka bir sunucuya göndermez.

Firefox, bu bilgileri bilgisayarınızdaki uygulamaya göndermek için kurulumda bir kez onayınızı ister.

### Eklentinin kendi istekleri

Eklenti yalnızca açık sayfanın bağlantılarına istek yapar:

- video listelerini (m3u8) okumak için,
- bağlantı listesinde dosya boyutunu ve türünü öğrenmek için,
- "siteyi tara" özelliğini kullandığınızda sayfaları okumak için,
- açılır penceredeki küçük resimleri göstermek için.

### Eklenti tarayıcıda ne saklar?

- Ayarlar: eşleşme anahtarı, otomatik yakalama, en küçük dosya boyutu, video düğmesi ve yakalanmayan siteler listesi.
- Sekmede yakalanan videoların listesi. Sekme kapanınca silinir.

### Uygulama hangi sunuculara bağlanır?

- İndirdiğiniz dosyaların sunucularına.
- GitHub'a (`github.com` ve GitHub'ın dosya sunucuları): açılıştan 30 saniye sonra ve 6 saatte bir yeni sürüm denetimi için. Bu istekte kişisel bilgi yoktur; GitHub, her sunucu gibi IP adresinizi görür.
- İlk YouTube veya X indirmesinde yt-dlp ve Deno araçlarını indirmek için GitHub'a (`api.github.com`, `github.com`). yt-dlp güncellemesi en çok günde bir denetlenir.
- yt-dlp, indirmek istediğiniz videonun sitesine (YouTube, X) bağlanır.
- `www.msftconnecttest.com` adresine, yalnızca Ayarlar'da vekil sunucu için "Test et" düğmesine bastığınızda.

Hakkında penceresindeki bağlantılar yalnızca tıkladığınızda tarayıcınızda açılır. Vekil sunucu ayarladıysanız bağlantılar onun üzerinden geçer.

### Uygulama bilgisayarınızda ne saklar?

Klasör: `%APPDATA%\idmalternative`

- `settings.json`: ayarlar.
- `downloads.json`: indirme listesi. Bitmemiş indirmelerin istek başlıkları (çerezler dahil) devam edebilmek için burada şifresiz durur. İndirme bitince ya da listeden silinince başlıklar da silinir.
- `logins.json`: kaydettiğiniz site girişleri ve vekil sunucu bilgileri. Parolalar Windows şifrelemesiyle (DPAPI) saklanır.
- `app.log`: olay ve hata günlüğü. Dosya adları ve site adresleri geçebilir.
- `tools`: yt-dlp ve Deno. `extension`: eklenti dosyalarının kopyası.

YouTube çerezleri yalnızca bellekte tutulur. yt-dlp çalışırken geçici bir dosyaya yazılır ve iş bitince silinir. İndirdiğiniz dosyalar seçtiğiniz klasöre kaydedilir.

### Verilerinizi silmek

Eklentiyi kaldırmak eklenti ayarlarını siler. Uygulamayı kaldırıp `%APPDATA%\idmalternative` klasörünü silmek uygulama verilerini siler.

### İletişim

Sorularınız için GitHub'da bir konu (issue) açın: [github.com/felicrutter/bar-downloader-releases/issues](https://github.com/felicrutter/bar-downloader-releases/issues)

## English

Last updated: 11 November 2026 (version 0.0.9)

Bar Downloader needs no account and shows no ads. It collects no usage data, analytics or crash reports. What the extension sends goes only to the Bar Downloader app on this computer. We run no server.

### What does the extension send, and where?

When you hand a download to Bar Downloader, the extension sends the following only to `http://127.0.0.1:27117`. This address is the app on your computer:

- the file address (URL) and file name,
- the address of the page the link is on (Referer),
- your browser's identification string (User-Agent),
- the browser's cookies for that address only, so that files behind a sign-in also download.

For YouTube addresses, only youtube.com cookies are sent. The app uses them only after you agree. The extension sends none of this to any other server.

Firefox asks once, at install, for your consent to send this data to the app on your computer.

### The extension's own requests

The extension only requests links of the open page:

- to read video playlists (m3u8),
- to find the size and type of files in the link list,
- to read pages when you use "crawl site",
- to show thumbnails in the popup.

### What does the extension keep in the browser?

- Settings: the pairing key, automatic capture, minimum file size, the video button and the list of sites not captured.
- The list of videos captured in a tab. It is deleted when the tab closes.

### Which servers does the app connect to?

- The servers of the files you download.
- GitHub (`github.com` and GitHub's file servers): 30 seconds after start and every 6 hours, to check for a new version. This request carries no personal data; like any server, GitHub sees your IP address.
- GitHub (`api.github.com`, `github.com`) on the first YouTube or X download, to fetch the yt-dlp and Deno tools. yt-dlp updates are checked at most once a day.
- yt-dlp connects to the site of the video you download (YouTube, X).
- `www.msftconnecttest.com`, only when you press "Test" for the proxy in Settings.

Links in the About window open in your browser only when you click them. If you set a proxy, connections go through it.

### What does the app keep on your computer?

Folder: `%APPDATA%\idmalternative`

- `settings.json`: settings.
- `downloads.json`: the download list. For unfinished downloads, the request headers (cookies included) are kept here unencrypted so the download can resume. They are deleted when the download finishes or is removed from the list.
- `logins.json`: the site logins and proxy details you save. Passwords are stored with Windows encryption (DPAPI).
- `app.log`: an event and error log. It can contain file names and site addresses.
- `tools`: yt-dlp and Deno. `extension`: a copy of the extension files.

YouTube cookies are kept in memory only. While yt-dlp runs they are written to a temporary file, which is deleted when the job ends. Downloaded files are saved to the folder you choose.

### Deleting your data

Removing the extension deletes its settings. Uninstalling the app and deleting the `%APPDATA%\idmalternative` folder deletes the app's data.

### Contact

For questions, open an issue on GitHub: [github.com/felicrutter/bar-downloader-releases/issues](https://github.com/felicrutter/bar-downloader-releases/issues)
