*  Bu hafta define kullanmadaki asıl hedef G sayısını tanımlamaktı. Bunu yaptıktan sonra ayrıca `float g = G;`  demeye gerek yok.
* `define`  ile tanımladığınız ifadeleri her ne kadar zorunlu olmasa da büyük harfle yazın. Çünkü bu ifade değişken değil, derleyici tarafından aşağıda her görüldüğü yere sanki bunu yazmışsınız gibi algılanıyor.
* Yalnızca belli katsayılar değil bazı ifadeler de `define` ile tanımlanabilir. Örnek vermek gerekirse ½g\*t^2 ifadesini bu şekilde yapanlar olmuş.
Yalnızca dikkat etmek gereken bazı noktalar var. 
Kullanımın `#define DIST(g,t) 0.5*(g)*(t)*(t)` şeklinde olması gerekiyor. Yoksa istenmeyen sonuçlarla karşılaşabiliriz. Yanlış örnek olarak aşağıdaki kodu çalıştırdığımızda 21 yazmasını beklerken 1+2*3+4=11 yazdırır.

```
  #define MULT(a,b) a*b
  ...
  cout << MULT(1+2, 3+4);
```

* `cout << 1/2;` dediğimizde sonuç 0'dır. Çünkü bu sayılar **int** yani tamsayı olarak algılanır. Bunu önlemek için şu yapılabilir:
`cout << 1./2;` 1. demek ile 1.0 demek aynı şey. Böyle dediğimizde 1 artık **double** olur ve 2'ye böldüğümüzde virgülden sonrasını atmaz.

*    *Scope of variable* dediğimiz bir olay var. Değişkenleri nerede gerekiyorsa orada tanımlayın. 
`main` fonksiyondan önce değişken tanımlayanlar olmuş, gerekmiyorsa bundan kaçının. [Scopes Hakkında Link](http://www.cplusplus.com/doc/tutorial/namespaces/)

* Kodda yazdığınız her satır sırayla çalışır. Dolayısıyla aşağıdaki kullanım hatalı:

```
float t;
float x = 0.5*G*t*t; // t belli değil!
cin >> t;
```
Bunun yerine şu yapılabilir:

```
float t, x;
cin >> t;
x = 1./2 * G * t*t;
```
