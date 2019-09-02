## CSS Pre-Processors İle Mixin Kullanımı

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







http://lesscss.org/features/#mixins-feature

