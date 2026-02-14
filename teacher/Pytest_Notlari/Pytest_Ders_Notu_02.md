# String Manipulation (String İşlemleri) - Detaylı Eğitim İçeriği

## 1. String Nedir ve Temel Özellikleri
w3ww3
String (metin), karakter dizilerini temsil eden Python veri tipidir.

**Temel Özellikler:**
- String'ler immutable (değiştirilemez) veri tipidir
- Tek tırnak ('), çift tırnak (") veya üçlü tırnak (""" veya ''') ile tanımlanır
- Unicode karakterleri destekler
- Indexleme ve dilimleme (slicing) yapılabilir
- Birçok built-in metot içerir

**Örnek:**
```python
name = "Python"
message = 'Merhaba Dünya'
multiline = """Bu bir
çok satırlı
metindir"""
```

## 2. String Oluşturma Yöntemleri

### a) Tek Tırnak:
```python
text = 'Python'
```

### b) Çift Tırnak:
```python
text = "Python"
```

### c) Üçlü Tırnak (Çok Satırlı):
```python
text = """Bu bir
çok satırlı
metindir"""
```

### d) Escape Karakterleri:
- `\n`: Yeni satır
- `\t`: Tab
- `\\`: Ters eğik çizgi
- `\'`: Tek tırnak
- `\"`: Çift tırnak
- `\r`: Satır başı
- `\b`: Backspace

### e) Raw String (r-string):
- Escape karakterlerini görmezden gelir
- Örnek: `path = r"C:\Users\Documents"`

## 3. String Indexleme ve Dilimleme

Python'da string'ler bir karakter dizisi gibi davranır ve her karakterin bir index'i vardır.

### a) Indexleme:
- İlk karakter index 0'dan başlar
- Negatif indexler sondan başlar (-1 son karakter)
- Örnek: `text[0]`, `text[-1]`

### b) Dilimleme (Slicing):
- **Syntax:** `string[start:end:step]`
- `start`: Başlangıç index (dahil)
- `end`: Bitiş index (hariç)
- `step`: Adım sayısı (varsayılan 1)

**Örnekler:**
```python
text[0:3]    # İlk 3 karakter
text[:3]     # Baştan 3. karaktere kadar
text[3:]     # 3. karakterden sona kadar
text[::2]    # Her 2 karakterden birini al
text[::-1]   # Tersine çevir
```

## 4. String Birleştirme ve Tekrarlama

### a) Birleştirme (+ operatörü):
```python
first = "Python"
last = "Programlama"
full = first + " " + last
```

### b) Tekrarlama (* operatörü):
```python
text = "Ha" * 3  # "HaHaHa"
```

### c) join() metodu:
```python
words = ["Python", "Programlama", "Dili"]
result = " ".join(words)  # "Python Programlama Dili"
```

## 5. String Metodları - Büyük/Küçük Harf

### a) upper():
Tüm karakterleri büyük harfe çevirir
```python
text.upper()  # "PYTHON"
```

### b) lower():
Tüm karakterleri küçük harfe çevirir
```python
text.lower()  # "python"
```

### c) capitalize():
İlk karakteri büyük, diğerlerini küçük yapar
```python
text.capitalize()  # "Python"
```

### d) title():
Her kelimenin ilk harfini büyük yapar
```python
text.title()  # "Python Programlama"
```


### e) swapcase():
Büyük harfleri küçük, küçük harfleri büyük yapar
```python
text.swapcase()  # "pYTHON"
```

## 6. String Metodları - Arama ve Kontrol

### a) find(substring):
Substring'in ilk bulunduğu index'i döner (-1 bulunamazsa)
```python
text.find("Py")  # 0
```

### b) index(substring):
find() gibi ama bulunamazsa hata verir
```python
text.index("Py")  # 0
```

### c) count(substring):
Substring'in kaç kez geçtiğini sayar
```python
text.count("n")  # 1
```

### d) startswith(prefix):
String belirtilen prefix ile başlıyor mu?
```python
text.startswith("Py")  # True
```

### e) endswith(suffix):
String belirtilen suffix ile bitiyor mu?
```python
text.endswith("on")  # True
```

## 7. String Metodları - Değiştirme

### a) replace(old, new):
Eski substring'i yeni ile değiştirir
```python
text.replace("Python", "Java")
```

### b) strip():
Başındaki ve sonundaki boşlukları kaldırır
```python
text.strip()
```

### c) lstrip():
Sadece başındaki boşlukları kaldırır
```python
text.lstrip()
```

### d) rstrip():
Sadece sonundaki boşlukları kaldırır
```python
text.rstrip()
```

## 8. String Metodları - Bölme ve Birleştirme

### a) split(separator):
String'i belirtilen ayırıcıya göre böler (liste döner)
```python
text.split(" ")  # ["Python", "Programlama"]
```

### b) splitlines():
String'i satırlara göre böler
```python
text.splitlines()
```

### c) join(iterable):
Liste veya tuple'ı string'e birleştirir
```python
" ".join(["Python", "Programlama"])
```

## 9. String Metodları - Formatlama ve Kontrol

### a) format():
String formatlama
```python
"{} {}".format("Python", "Programlama")
```

### b) f-string (Python 3.6+):
Modern formatlama yöntemi
```python
f"{name} {age} yaşında"
```

### c) isalnum():
Sadece harf ve rakam içeriyor mu?
```python
text.isalnum()
```

### d) isalpha():
Sadece harf içeriyor mu?
```python
text.isalpha()
```

### e) isdigit():
Sadece rakam içeriyor mu?
```python
text.isdigit()
```

### f) isspace():
Sadece boşluk karakterleri içeriyor mu?
```python
text.isspace()
```

### g) isupper():
Tüm karakterler büyük harf mi?
```python
text.isupper()
```

### h) islower():
Tüm karakterler küçük harf mi?
```python
text.islower()
```

## 10. String Formatlama Yöntemleri

### a) % Formatlama (Eski Yöntem):
```python
"İsim: %s, Yaş: %d" % ("Ahmet", 25)
```

### b) .format() Metodu:
```python
"İsim: {}, Yaş: {}".format("Ahmet", 25)
"İsim: {0}, Yaş: {1}".format("Ahmet", 25)
"İsim: {name}, Yaş: {age}".format(name="Ahmet", age=25)
```

### c) f-string (Önerilen):
```python
name = "Ahmet"
age = 25
f"İsim: {name}, Yaş: {age}"
f"Yaşın 2 katı: {age * 2}"
f"Formatlı sayı: {price:.2f}"
```

## 11. String İşlemleri - Uzunluk ve Karakter İşlemleri

### a) len():
String uzunluğunu döner
```python
len(text)  # 6
```

### b) max():
En büyük karakteri döner (ASCII değerine göre)
```python
max(text)  # 'y'
```

### c) min():
En küçük karakteri döner
```python
min(text)  # 'P'
```

### d) ord():
Karakterin ASCII/Unicode değerini döner
```python
ord('A')  # 65
```

### e) chr():
ASCII/Unicode değerinden karakter üretir
```python
chr(65)  # 'A'
```

## 12. String İşlemleri - Özel Kullanımlar

- String çoğaltma ve birleştirme
- String karşılaştırma (==, !=, <, >)
- String içinde arama ve değiştirme
- String temizleme ve düzenleme
- String validasyonu
- String parsing (ayrıştırma)

## 13. Geçici ve Kalıcı Değişim - Önemli Konsept

Python'da string'ler **immutable** (değiştirilemez) olduğu için, tüm string metodları **yeni bir string döndürür**. Orijinal string asla değişmez.

### Geçici Değişim (Orijinal String Değişmez)

String metodları çağrıldığında orijinal string'i değiştirmez, sadece yeni bir string döndürür:

```python
text = "Python"
result = text.upper()  # Yeni string döndürür
print(text)    # "Python" (orijinal değişmedi)
print(result)  # "PYTHON" (yeni string)
```

**Geçici değişim yapan metodlar (örnekler):**
- `upper()`, `lower()`, `capitalize()`, `title()`, `swapcase()`
- `strip()`, `lstrip()`, `rstrip()`
- `replace()`
- `split()`, `splitlines()`
- Tüm string metodları aslında geçici değişim yapar

### Kalıcı Değişim (Değişkene Yeniden Atama)

Kalıcı değişim için, metodun döndürdüğü yeni string'i aynı değişkene atamak gerekir:

```python
text = "Python"
text = text.upper()  # Yeni string'i aynı değişkene atadık
print(text)  # "PYTHON" (artık kalıcı olarak değişti)
```

**Kalıcı değişim örnekleri:**

```python
# Örnek 1: Büyük harfe çevirme
text = "python"
text = text.upper()  # Kalıcı değişim
print(text)  # "PYTHON"

# Örnek 2: Boşlukları temizleme
text = "  Python  "
text = text.strip()  # Kalıcı değişim
print(text)  # "Python"

# Örnek 3: Değiştirme
text = "Python Programlama"
text = text.replace("Python", "Java")  # Kalıcı değişim
print(text)  # "Java Programlama"

# Örnek 4: Birden fazla işlem
text = "  python programlama  "
text = text.strip().title()  # Önce strip, sonra title
print(text)  # "Python Programlama"
```

### Önemli Notlar

1. **String'ler immutable'dır:** Orijinal string asla değişmez
2. **Metodlar yeni string döndürür:** Her metod çağrısı yeni bir string oluşturur
3. **Kalıcı değişim için atama gerekir:** `text = text.method()` şeklinde kullanılmalı
4. **Zincirleme işlemler:** Birden fazla metodu zincirleyebilirsiniz: `text.strip().upper()`

### Karşılaştırma Tablosu

| İşlem | Geçici Değişim | Kalıcı Değişim |
|-------|----------------|----------------|
| **Kod** | `text.upper()` | `text = text.upper()` |
| **Orijinal String** | Değişmez | Değişmez (ama değişken yeni değeri tutar) |
| **Sonuç** | Yeni string döndürür | Yeni string döndürür ve değişkene atar |
| **Kullanım** | `print(text.upper())` | `text = text.upper()` |

### Pratik Örnekler

```python
# Geçici değişim - sadece görüntüleme
text = "Python"
print(text.upper())  # "PYTHON" - sadece yazdırır
print(text)          # "Python" - orijinal değişmedi

# Kalıcı değişim - değişkene atama
text = "Python"
text = text.upper()  # Yeni değeri değişkene atadık
print(text)          # "PYTHON" - artık kalıcı olarak değişti

# Zincirleme işlemler (geçici)
text = "  python  "
result = text.strip().upper().replace("PYTHON", "JAVA")
print(result)  # "JAVA"
print(text)    # "  python  " (orijinal değişmedi)

# Zincirleme işlemler (kalıcı)
text = "  python  "
text = text.strip().upper().replace("PYTHON", "JAVA")
print(text)    # "JAVA" (artık kalıcı)
```

