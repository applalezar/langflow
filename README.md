<!-- markdownlint-disable MD030 -->

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./docs/static/img/langflow-logo-color-blue-bg.svg">
  <img src="./docs/static/img/langflow-logo-color-black-solid.svg" alt="Langflow logosu">
</picture>

[![Sürüm Notları](https://img.shields.io/github/release/langflow-ai/langflow?style=flat-square)](https://github.com/langflow-ai/langflow/releases)
[![PyPI - Lisans](https://img.shields.io/badge/license-MIT-orange)](https://opensource.org/licenses/MIT)
[![PyPI - İndirmeler](https://img.shields.io/pypi/dm/langflow?style=flat-square)](https://pypistats.org/packages/langflow)
[![Twitter](https://img.shields.io/twitter/url/https/twitter.com/langflow-ai.svg?style=social&label=Follow%20%40Langflow)](https://twitter.com/langflow_ai)
[![YouTube Kanalı](https://img.shields.io/youtube/channel/subscribers/UCn2bInQrjdDYKEEmbpwblLQ?label=Abone%20Ol)](https://www.youtube.com/@Langflow)
[![Discord Sunucusu](https://img.shields.io/discord/1116803230643527710?logo=discord&style=social&label=Kat%C4%B1l)](https://discord.gg/EqksyE2EX9)
[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/langflow-ai/langflow)

[Langflow](https://langflow.org), yapay zeka destekli ajanlar ve iş akışları oluşturmak ve dağıtmak için güçlü bir platformdur. Geliştiricilere hem görsel bir yazma deneyimi hem de her iş akışını herhangi bir framework veya yığın üzerine inşa edilmiş uygulamalara entegre edilebilen bir araca dönüştüren yerleşik API ve MCP sunucuları sağlar. Langflow pil dahil gelir ve tüm büyük LLM'leri, vektör veritabanlarını ve büyüyen bir yapay zeka araçları kütüphanesini destekler.

## ✨ Öne Çıkan Özellikler

- Hızlıca başlamak ve yinelemek için **görsel oluşturucu arayüzü**.
- **Kaynak koda erişim**, Python kullanarak herhangi bir bileşeni özelleştirmenizi sağlar.
- Adım adım kontrolle akışlarınızı anında test etmek ve geliştirmek için **etkileşimli oyun alanı**.
- Konuşma yönetimi ve geri alımla **çok ajanlı orkestrasyon**.
- **API olarak dağıtın** veya Python uygulamaları için JSON olarak dışa aktarın.
- **MCP sunucusu olarak dağıtın** ve akışlarınızı MCP istemcileri için araçlara dönüştürün.
- LangSmith, LangFuse ve diğer entegrasyonlarla **gözlemlenebilirlik**.
- **Kurumsal düzeyde** güvenlik ve ölçeklenebilirlik.

## 🖥️ Langflow Desktop

Langflow Desktop, Langflow'a başlamanın en kolay yoludur. Tüm bağımlılıklar dahildir, bu nedenle Python ortamlarını yönetmenize veya paketleri manuel olarak yüklemenize gerek yoktur.
Windows ve macOS için kullanılabilir.

[📥 Langflow Desktop'ı İndirin](https://www.langflow.org/desktop)

## ⚡️ Hızlı Başlangıç

### Yerel olarak yükleyin (önerilen)

Python 3.10–3.13 ve [uv](https://docs.astral.sh/uv/getting-started/installation/) (önerilen paket yöneticisi) gerektirir.

#### Kurulum

Yeni bir dizinden şunu çalıştırın:
```shell
uv pip install langflow -U
```

En son Langflow paketi yüklenir.
Daha fazla bilgi için [Langflow OSS Python paketini yükleyin ve çalıştırın](https://docs.langflow.org/get-started-installation#install-and-run-the-langflow-oss-python-package) bölümüne bakın.

#### Çalıştırma

Langflow'u başlatmak için şunu çalıştırın:
```shell
uv run langflow run
```

Langflow http://127.0.0.1:7860 adresinde başlar.

İşte bu kadar! Langflow ile oluşturmaya hazırsınız! 🎉

## 📦 Diğer Kurulum Seçenekleri

### Kaynaktan çalıştırma
Bu depoyu klonladıysanız ve katkıda bulunmak istiyorsanız, depo kökünden şu komutu çalıştırın:
```shell
make run_cli
```
Daha fazla bilgi için [DEVELOPMENT.md](./DEVELOPMENT.md) dosyasına bakın.

### Docker
Varsayılan ayarlarla bir Langflow konteyneri başlatın:
```shell
docker run -p 7860:7860 langflowai/langflow:latest
```
Langflow http://localhost:7860/ adresinde kullanılabilir.
Yapılandırma seçenekleri için [Docker dağıtım kılavuzuna](https://docs.langflow.org/deployment-docker) bakın.

> [!CAUTION]
> - Kullanıcılar [CVE-2025-68477](https://github.com/langflow-ai/langflow/security/advisories/GHSA-5993-7p27-66g5) ve [CVE-2025-68478](https://github.com/langflow-ai/langflow/security/advisories/GHSA-f43r-cc68-gpx4)'e karşı korunmak için Langflow >= 1.7.1 sürümüne güncellemelidir.
> - Langflow sürüm 1.7.0'da, yükseltme yapılırken kalıcı durumun (akışlar, projeler ve global değişkenler) bulunamadığı kritik bir hata vardır. Sürüm 1.7.0 geri çekildi ve bu hatanın düzeltmesini içeren sürüm 1.7.1 ile değiştirildi. Sürüm 1.7.0'a **GÜNCELLEME YAPMAYIN**. Bunun yerine doğrudan sürüm 1.7.1'e yükseltin.
> - Langflow sürümleri 1.6.0 ile 1.6.3 arasında `.env` dosyalarının okunmadığı ve potansiyel güvenlik açıklarına neden olabilen kritik bir hata vardır. Yapılandırma için `.env` dosyaları kullanıyorsanız bu sürümlere **GÜNCELLEME YAPMAYIN**. Bunun yerine, bu hatanın düzeltmesini içeren 1.6.4 sürümüne yükseltin.
> - Langflow Desktop'ın Windows kullanıcıları, Langflow sürüm 1.6.0'a yükseltmek için uygulama içi güncelleme özelliğini **kullanmamalıdır**. Yükseltme talimatları için [Windows Desktop güncelleme sorunu](https://docs.langflow.org/release-notes#windows-desktop-update-issue) bölümüne bakın.
> - Kullanıcılar [CVE-2025-3248](https://nvd.nist.gov/vuln/detail/CVE-2025-3248)'e karşı korunmak için Langflow >= 1.3 sürümüne güncellemelidir
> - Kullanıcılar [CVE-2025-57760](https://github.com/langflow-ai/langflow/security/advisories/GHSA-4gv9-mp8m-592r)'a karşı korunmak için Langflow >= 1.5.1 sürümüne güncellemelidir
>
> Güvenlik bilgileri için [Güvenlik Politikamıza](./SECURITY.md) ve [Güvenlik Danışma Bilgilerine](https://github.com/langflow-ai/langflow/security/advisories) bakın.

## 🚀 Dağıtım

Langflow tamamen açık kaynaklıdır ve tüm büyük dağıtım bulutlarına dağıtabilirsiniz. Langflow'un nasıl dağıtılacağını öğrenmek için [Langflow dağıtım kılavuzlarımıza](https://docs.langflow.org/deployment-overview) bakın.

## ⭐ Güncel Kalın

Yeni sürümlerden anında haberdar olmak için GitHub'da Langflow'u yıldızlayın.

![Langflow'u Yıldızlayın](https://github.com/user-attachments/assets/03168b17-a11d-4b2a-b0f7-c1cce69e5a2c)

## 👋 Katkıda Bulunun

Her seviyeden geliştiricinin katkılarını memnuniyetle karşılıyoruz. Katkıda bulunmak isterseniz, lütfen [katkı kılavuzumuzu](./CONTRIBUTING.md) kontrol edin ve Langflow'u daha erişilebilir hale getirmeye yardımcı olun.

---

[![Yıldız Geçmişi Grafiği](https://api.star-history.com/svg?repos=langflow-ai/langflow&type=Timeline)](https://star-history.com/#langflow-ai/langflow&Date)

## ❤️ Katkıda Bulunanlar

[![langflow katkıda bulunanlar](https://contrib.rocks/image?repo=langflow-ai/langflow)](https://github.com/langflow-ai/langflow/graphs/contributors)
