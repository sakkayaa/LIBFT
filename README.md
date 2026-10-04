# libft

> **C ile temel kütüphane fonksiyonlarını yeniden yazma projesi**  
> Standart C fonksiyonlarının davranışını anlamak, bellek yönetimini uygulamak ve yeniden kullanılabilir bir statik kütüphane oluşturmak için hazırlanmıştır.

## Proje hakkında

`libft`, C dilinde sık kullanılan karakter kontrolü, string, bellek ve dosya tanımlayıcısına yazdırma fonksiyonlarının yeniden uygulamalarını içeren bir kütüphanedir. Proje; pointer kullanımı, buffer yönetimi, sınır durumları ve fonksiyon davranışlarını dikkatle ele alma pratiği sunar.

Derleme sonunda `libft.a` statik kütüphanesi oluşturulur. Böylece fonksiyonlar başka C projelerinde tekrar kullanılabilir.

## Öne çıkanlar

- **Karakter kontrolleri:** harf, rakam, alfanümerik ve yazdırılabilir karakter kontrolleri
- **String işlemleri:** uzunluk, kopyalama, birleştirme, arama ve karşılaştırma
- **Bellek işlemleri:** doldurma, kopyalama, taşıma, arama ve sıfırlama
- **Dönüşüm ve ayırma:** `atoi`, `calloc`, `strdup`
- **Dosya tanımlayıcısına çıktı:** karakter, string, satır ve sayı yazdırma
- **Statik kütüphane:** Makefile ile `libft.a` üretimi

## Fonksiyonlar

| Alan | Fonksiyonlar |
|---|---|
| Karakter kontrolü ve dönüşümü | `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`, `ft_tolower`, `ft_toupper` |
| String ölçme, kopyalama ve birleştirme | `ft_strlen`, `ft_strlcpy`, `ft_strlcat`, `ft_strdup` |
| String arama ve karşılaştırma | `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr` |
| Bellek işlemleri | `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`, `ft_calloc` |
| Sayı dönüştürme | `ft_atoi` |
| Dosya tanımlayıcısına yazdırma | `ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd` |

Fonksiyon bildirimleri `libft.h` başlık dosyasında yer alır.

## Gereksinimler

- C derleyicisi (`gcc` veya uyumlu bir derleyici)
- `make`

## Derleme

Depoyu klonlayıp proje klasörüne geçin:

```bash
git clone <repository-url>
cd LIBFT-main
```

Statik kütüphaneyi oluşturun:

```bash
make
```

Başarılı derlemede proje klasöründe `libft.a` oluşur.

## Başka bir projede kullanma

`libft.h` dosyasını projenize dahil edin ve uygulamanızı statik kütüphane ile birlikte derleyin:

```c
#include "libft.h"

int main(void)
{
    ft_putendl_fd("Hello, libft!", 1);
    return (0);
}
```

```bash
cc -Wall -Wextra -Werror -I/path/to/libft \
  main.c /path/to/libft/libft.a -o app
```

`/path/to/libft` kısmını `libft.h` ve `libft.a` dosyalarının bulunduğu konumla değiştirin.

## Makefile komutları

| Komut | Açıklama |
|---|---|
| `make` | `libft.a` kütüphanesini oluşturur |
| `make clean` | Nesne dosyalarını siler |
| `make fclean` | Nesne dosyalarıyla birlikte `libft.a` dosyasını siler |
| `make re` | Temiz derleme yapar |

## Öğrenme çıktıları

Bu çalışma; C standart kütüphanesinin temel davranışlarını inceleme, pointer ve dinamik bellekle çalışma, fonksiyonları modüler tasarlama ve derleme sürecini Makefile ile yönetme konularındaki pratiği gösterir.

## Geliştiren

**Sedef Akkaya**  
GitHub: [GitHub](https://github.com/sakkayaa) · LinkedIn: [Sedef Akkaya](https://www.linkedin.com/in/sedef-akkaya-0a5580228/)

---

*C temellerini anlayarak inşa et. Küçük fonksiyonlar, sağlam altyapı.*
