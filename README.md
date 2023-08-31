# Sık Kullanılan Git Komutları

Git yeni kurulduysa temel ayarlar yapmamız gerekiyor. Bunlardan bir tanesi Giti kullanan kişinin ad ve soyadının yazılmasıdır. Bunun amacı yazılan kodun kimin yazdığını kolayca göstermektir.  Bunu ayarlamanın yolu temel ayarlardaki 1. adımdır. Diğer bir ayarımız ise e-posta ayarı. Burada kullandığınız e-posta adresinin GitHub hesabınızda kullandığınız e-posta ile aynı olmasına dikkat edin.

## Temel Ayarlar
1. `git config --global user.name "Ad Soyad"` Kullanıcı adınızı ayarlar.
2. `git config --global user.email "e-posta@example.com"` E-posta adresinizi ayarlar.

Ayarları yaptıktan sonra bilgisayardaki projemizde ilk defa Git kullanılacaksa aşağıdaki 1. adım ile Git initialize edilmelidir. Ama eğer hali hazırda GitHubda bir proje varsa o halde 1. adıma ihtiyacınız yok. Bunun yerine 2. adımı takip ederek GitHubdaki projeyi klonlayabilirsiniz.

## Depo Oluşturma ve Klonlama
1. `git init` Yeni bir Git deposu oluşturur.
2. `git clone <repo_url>` Uzak bir depoyu yerel makineye klonlar.

Bir önceki aşamada 1. yol tercih edilip `git init` komutu kullanıldıysa GitHubdaki projeyi bağlamanız gerekmektedir. Bunu aşağıdaki 1. adımda yapabilirsiniz. Projenin repo ile bağlantısını yaptıktan sonra ana branch ayarı yapmamız gerekiyor. Hem GitHuba hem de Gite kullandığımız branchın main olduğunu söylemek için 2. adımı takip edebilirsiniz

## Repo bağlantısı
1. `git remote add origin <repo_url>` Uzak depoyu ekler.
2. `git branch -M main` Ana branch ayarı

