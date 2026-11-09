# KoruGAN

KoruGAN, uygulama dağıtımı ve izolasyonu için bir sistemdir.

[English](README.md) | [Türkçe](README.tr.md)

## Konteynerler ve alternatifleri

Docker yaygın kullanılan bir konteyner ekosistemidir; ancak bileşenleri ve ürünleri farklı işlevlere ve lisanslara sahiptir:

- **Docker Engine**, başta Linux'ta kullanılan açık kaynaklı konteyner motorudur.
- **Docker Desktop**, Docker'ın macOS, Windows ve Linux için sunduğu masaüstü uygulamasıdır. Açık kaynaklı bileşenler içerir; ancak Docker Desktop'ın kendisi Docker'ın abonelik koşullarıyla dağıtılır.
- **İmajlar**, bir uygulamayı ve bağımlılıklarını paketler; **konteynerler** bu imajlardan çalışan örneklerdir.

Aşağıdaki projelerin tümü Docker'ın doğrudan yerine geçmez. Bazıları imaj oluşturur, bazıları konteyner çalıştırır; bazıları masaüstü arayüzü ya da Kubernetes'e özgü çalışma zamanı sunar.

### Açık kaynaklı projeler

| Proje | Kategori | Lisans | Uygun olduğu kullanım |
| --- | --- | --- | --- |
| [Docker Engine](https://docs.docker.com/engine/) | Konteyner motoru | Apache-2.0 | Linux'ta Docker CLI, daemon ve konteyner iş akışı |
| [Podman](https://podman.io/docs) | Konteyner motoru | Apache-2.0 | Daemon olmadan konteyner yönetimi; rootless iş akışları dahil |
| [containerd](https://containerd.io/) | Konteyner çalışma zamanı | Apache-2.0 | Kubernetes gibi platformların kullandığı daha alt düzey çalışma zamanı; Docker Desktop'ın tam karşılığı değildir |
| [Buildah](https://buildah.io/) | İmaj oluşturucu | Apache-2.0 | Docker daemon gerektirmeden OCI imajları oluşturma |
| [CRI-O](https://cri-o.io/) | Kubernetes çalışma zamanı | Apache-2.0 | Kubernetes için konteyner çalıştırma; genel amaçlı Docker alternatifi değildir |
| [LXC](https://linuxcontainers.org/lxc/introduction/) | Sistem konteynerleri | LGPL-2.1 | Hafif Linux sistem konteynerleri; OCI uygulama konteynerlerinden farklı bir model |
| [Podman Desktop](https://podman-desktop.io/) | Masaüstü arayüzü | Apache-2.0 | Podman ve diğer konteyner araçlarını grafik arayüzle yönetme |
| [Rancher Desktop](https://rancherdesktop.io/) | Masaüstü ortamı | Apache-2.0 | containerd veya Moby ile yerel geliştirme; isteğe bağlı Kubernetes |
| [Colima](https://github.com/abiosoft/colima) | Yerel konteyner ortamı | MIT | Özellikle macOS'ta hafif, komut satırından yönetilen konteyner ortamı |

### Tescilli veya ticari masaüstü ürünleri

| Ürün | Platformlar | Lisans bilgisi |
| --- | --- | --- |
| [Docker Desktop](https://docs.docker.com/subscription-billing/desktop-license/) | macOS, Windows, Linux | Docker Desktop tescilli bir üründür ve açık kaynaklı bileşenler içerir. Docker'ın güncel koşulları kişisel kullanım, eğitim, ticari olmayan açık kaynak projeleri ve 250'den az çalışanı **ve** yıllık geliri 10 milyon ABD dolarından düşük küçük işletmeler için ücretsiz kullanıma izin verir. Diğer ticari kullanımlar ve kamu kurumları için ücretli abonelik gerekir. |
| [OrbStack](https://orbstack.dev/) | macOS | Tescilli bir masaüstü ürünüdür. Özellikle kurumsal kullanımda, benimsemeden önce güncel lisans ve fiyatlandırma koşullarını inceleyin. |

Docker Engine ve Docker Desktop aynı lisans koşullarına tabi değildir. Docker'ın abonelik koşulları Docker Desktop için geçerlidir; Docker, Docker Engine ve Moby açık kaynak projelerinin lisans koşullarının değişmediğini belirtir. Kullanacağınız ürün ve kullanım biçimi için güncel lisans ve abonelik koşullarını mutlaka inceleyin.

### Araç seçimi

- Özellikle Linux'ta, standart Docker Engine ve CLI iş akışını istiyorsanız **Docker Engine**'i tercih edin.
- Daemon kullanmayan veya rootless iş akışları için **Podman**'ı değerlendirin; Docker API'sine ya da Compose'a bağlı araçların uyumluluğunu ayrıca sınayın.
- **containerd** veya **CRI-O**'yu doğrudan masaüstü alternatifi olarak değil, Kubernetes altyapısı seçerken değerlendirin.
- İmaj oluşturmak için **Buildah**'ı; OCI uygulama konteynerleri yerine Linux sistem konteynerleri gerekiyorsa **LXC**'yi değerlendirin.
- Grafik arayüzlü yerel bir ortam için **Podman Desktop**, **Rancher Desktop**, **Docker Desktop** ve **OrbStack** ürünlerini işletim sistemi ve lisans gereksinimlerinize göre karşılaştırın.

### Lisans

Copyright (C) 2026-2027 PSD Authors

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published
by the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.

See [CHANGELOG.md](CHANGELOG.md) for the project history.

Proje geçmişi için [CHANGELOG.md](CHANGELOG.md) dosyasına bakın.
