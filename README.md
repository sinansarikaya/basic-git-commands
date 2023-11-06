# Sık Kullanılan Git Komutları

Git yeni kurulduysa temel ayarlar yapmamız gerekiyor. Bunlardan bir tanesi Giti kullanan kişinin ad ve soyadının yazılmasıdır. Bunun amacı yazılan kodun kimin yazdığını kolayca göstermektir.  Bunu ayarlamanın yolu temel ayarlardaki 1. adımdır. Diğer bir ayarımız ise e-posta ayarı. Burada kullandığınız e-posta adresinin GitHub hesabınızda kullandığınız e-posta ile aynı olmasına dikkat edin.

## Temel Ayarlar
1. `git config --global user.name "Ad Soyad"` Adınızı ve Soyadınızı ayarlar.
2. `git config --global user.email "e-posta@example.com"` E-posta adresinizi ayarlar.

Ayarları yaptıktan sonra bilgisayardaki projemizde ilk defa Git kullanılacaksa aşağıdaki 1. adım ile Git initialize edilmelidir. Ama eğer hali hazırda GitHubda bir proje varsa o halde 1. adıma ihtiyacınız yok. Bunun yerine 2. adımı takip ederek GitHubdaki projeyi klonlayabilirsiniz.

## Depo Oluşturma ve Klonlama
1. `git init` Yeni bir Git deposu oluşturur.
2. `git clone <repo_url>` Uzak bir depoyu yerel makineye klonlar.

Bir önceki aşamada 1. yol tercih edilip `git init` komutu kullanıldıysa GitHubdaki projeyi bağlamanız gerekmektedir. Bunu aşağıdaki 1. adımda yapabilirsiniz. Projenin repo ile bağlantısını yaptıktan sonra ana branch ayarı yapmamız gerekiyor. Hem GitHuba hem de Gite kullandığımız branchın main olduğunu söylemek için 2. adımı takip edebilirsiniz

## Repo bağlantısı
1. `git remote add origin <repo_url>` Uzak depoyu ekler.
2. `git branch -M main` Ana branch ayarı
3. `git remote -v` Bağlı olduğu repoyu gösterir.

Takım halinde çalışmalar yapılıyorsa çalışmalara branchlar dahil edilmelidir. Farklı branchlarda çalışmak kod çakışmasını engeller. Branch olusturmak için aşağıdaki 1. adımı uygulayınız. 1. adımda yeni bir branch oluşturacaksınız. Bu branchın oluşup oluşmadığını 2. adımı takip ederek görebilirsiniz. Ayrıca 2. adımda listelenen branchlardan bir tanesinin adı yeşil renkte olur. Bunun anlamı şuan yeşil yazılan branchta çalışıyor olmanızdır. Olusturduğunuz brancha geçmek için 3. adımı takip ediniz.

## Branch İşlemleri
1. `git branch <branch_adı>`  Yeni bir dal oluşturur.
2. `git branch`: Mevcut dalları listeler.
3. `git checkout <branch_adı>` Bir dala geçiş yapar.

Yukarıdaki işlemler bittiğinde artık çalışmaya hazırsınız demektir. Öncelikle projeniz üzerindeki görevinizi yapıp kodlarınızı yazmalısınız. Daha sonra yaptığınız güncellemeleri GitHuba göndermek için gerekli adımları takip etmelisiniz. Aşağıdaki 1. komut ile değişiklik yaptığınız bütün dosyaları sisteme bildirirsiniz. 2. adımda yaptığınız değişiklikleri kısa bir ve İngilizce bir dille açıklamanız gerekir.  İngilizce olması zorunlu değildir ancak piyasada bu şekilde kullanılır. 3. adımda ise gönderilmeye hazır dosyaları kontrol edebilirsiniz. Bu adım isteğe bağlıdır. 4. adımda dosyalarımızı uzak sunucuya gönderiyoruz. Eğer çalışmakta olduğumuz branch ile ilk defa dosya gönderimi yapıyorsak 4. yol izlenir ama daha önce gönderim yapılduysa 5. yolu izleyebilirsiniz. 4. yol daima çalışır.

## Temel İşlemler
1. `git add .` Değişiklikleri göndermek için sisteme bildirir.
2. `git commit -m "Açıklama"` Hazırlanan değişiklikleri bir "commit" olarak kaydeder.
3. `git status` Depodaki değişikliklerin durumunu gösterir.
4. `git push -u origin <branch_adı>` Yerel "commit"leri uzak sunucuya gönderir bu komutu ilk defa push yapıyorsanız kullanın.
5. `git push` İlk push için 4. seçeneği 1 kere kullandıktan sonra her zaman bu seçeneği kullanarak push yapabilirsiniz.

