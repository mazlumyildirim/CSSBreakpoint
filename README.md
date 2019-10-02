## CSS Pre-Processors(LESS) ve Mixin Kullanımı


### Genel LESS kullanımı

### Nedir Mixin ?

> Kodlarda tekrarı önlemek, yönetebilirliği arttırmak ve kodu kısmen nesneleştirmek için oluşturulan, tekrar kullanılabilir özel tanımlanmış kod gruplarıdır.

Mixin'ler ile ilgi olarak örnek verecek olursak;

```
.box {
    border: 1px solid rgba(34, 255, 21, .6);
    box-shadow: 2px 10px 8px 0 rgba(34, 255, 21, .3);
    max-width: 250px;
    width: 100%;
    height: 400px;
    padding: 30px 40px
}
  
.product__item {
    background: #f4f6f6;
    margin-bottom: 20px;
    .box();
}
``` 

Yukardaki kod bloğunda ufak bir mixin örneği vermiş olduk.

###### Parametre belirterek kullanım

```
.absolute (@left, @top: 10px){
    position: absolute;
    top: @top;
    left: @left;
}

.block {
    .absolute(100px, 25px);
}

```

###### Fonksiyon olarak kullanım

```
.block {
    background: fadeout(red, 60%);
}

```

###### İşlemler

```
.block {
    margin: 5px * 2;
}

&&

.block {
    width: (100% - 20px) / 2;
}

```


###### Extend kullanım 

>  Extend bir miras alma yöntemidir. Benzer kodlar diğer seçicilerin içine dahil etmek için kullanılır. Bunu “@extend miras-alinanin-ismi” diyerek yapıyoruz.
Örn;
```
.button-base {
   margin: 2px;
   radius: 2px;
}

.error-base {
   background-color: red;
}

.error-button {
   @extend .button-base;
   @extend .error-base;
}

```

Devam eden Döküman




http://lesscss.org/features/#mixins-feature

