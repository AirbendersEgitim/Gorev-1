# Gorev-1
Bu haftaki görev `define` `cin` `cout` kullanımı üzerine. [DikkatEdilmesiGerekenler](https://github.com/AirbendersEgitim/Gorev-1/blob/main/DikkatEdilmesiGerekenler.md) adlı dosyayı da okursanız güzel olur.

Hedef: Serbest düşüşe bırakılan cismin t saniyede alacağı mesafeyi bulmak.

- Girdi: t (saniye)

- Çıktı: x (metre)

g = 9.80665 (m/s^2) alabilirsiniz.

-------
DevC++ kullananlar için Tools/Compiler Options.../General/Add the following commands when calling the linker: kısmına şunu yapıştırıp uyarı mesajları ve C++11'i aktifleştirebilirsiniz:


    -static-libgcc -Wall -Wextra -Wpedantic -O2 -std=c++11
