# calorie-counter

## Table of JavaScript Methods

| Method                  | Description |
|-------------------------|-------------|
| `.replace()`            | Mengganti bagian dari string dengan nilai baru berdasarkan pola yang diberikan. Bisa mengganti hanya satu atau semua kemunculan dalam string. Bisa digunakan dengan ekspresi reguler untuk pencarian yang lebih fleksibel. |
| `.match()`              | Mencocokkan string dengan ekspresi reguler dan mengembalikan hasil dalam bentuk array jika ada kecocokan, atau `null` jika tidak ditemukan. Cocok untuk ekstraksi data dari teks berdasarkan pola tertentu. |
| `.insertAdjacentHTML()` | Menyisipkan HTML ke dalam elemen pada posisi yang ditentukan (`beforebegin`, `afterbegin`, `beforeend`, `afterend`) tanpa mengganggu elemen yang sudah ada. Berguna untuk menyisipkan elemen baru ke dalam halaman secara dinamis. |
| `.preventDefault()`     | Mencegah perilaku default dari suatu event, seperti mencegah pengiriman formulir, navigasi tautan, atau perilaku bawaan elemen lain. Biasanya digunakan dalam event handler untuk mengontrol interaksi pengguna dengan lebih baik. |
| `Math.abs()`            | Mengembalikan nilai absolut dari suatu angka, menghilangkan tanda negatif jika ada. Berguna dalam perhitungan matematika ketika hanya nilai absolut yang dibutuhkan. |
| `Number()`              | Mengonversi nilai dari tipe lain (seperti string atau boolean) menjadi angka. Jika nilai tidak bisa dikonversi, hasilnya adalah `NaN` (Not a Number). Digunakan untuk memastikan input berupa angka sebelum dilakukan operasi matematika. |
| `Array.from()`          | Membuat array baru dari objek yang mirip array atau iterable, seperti `NodeList`, `arguments`, atau string. Bisa digunakan dengan fungsi mapping untuk transformasi elemen saat konversi. Sangat berguna dalam manipulasi DOM dan konversi struktur data. |

## Example Usage

### `.replace()`
```javascript
const text = "Hello, world!";
const newText = text.replace("world", "JavaScript");
console.log(newText); // "Hello, JavaScript!"

// Menggunakan ekspresi reguler untuk mengganti semua kemunculan
const sentence = "foo bar foo";
console.log(sentence.replace(/foo/g, "baz")); // "baz bar baz"
```

### `.match()`
```javascript
const sentence = "The rain in Spain stays mainly in the plain.";
const result = sentence.match(/ain/g);
console.log(result); // ["ain", "ain", "ain", "ain"]
```

### `.insertAdjacentHTML()`
```javascript
const div = document.getElementById("container");
div.insertAdjacentHTML("beforeend", "<p>Hello, world!</p>");
```

### `.preventDefault()`
```javascript
document.querySelector("a").addEventListener("click", function(event) {
  event.preventDefault(); // Mencegah navigasi
  console.log("Link clicked but not followed!");
});
```

### `Math.abs()`
```javascript
console.log(Math.abs(-10)); // 10
console.log(Math.abs(5.5)); // 5.5
console.log(Math.abs(-3.14)); // 3.14
```

### `Number()`
```javascript
console.log(Number("42")); // 42
console.log(Number("3.14")); // 3.14
console.log(Number(true)); // 1
console.log(Number(false)); // 0
console.log(Number("hello")); // NaN
```

### `Array.from()`
```javascript
const str = "hello";
const letters = Array.from(str);
console.log(letters); // ["h", "e", "l", "l", "o"]

// Mengubah NodeList menjadi Array
const nodeList = document.querySelectorAll("p");
const paragraphs = Array.from(nodeList);
console.log(paragraphs); // Array dari elemen <p>
```

