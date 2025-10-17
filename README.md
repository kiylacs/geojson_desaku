# geojson_desaku
Ringkasan:
- File ini berformat GeoJSON dengan tipe FeatureCollection.
- Terdapat 229 fitur di dalamnya.
- Jenis geometri yang digunakan ada Point (titik koordinat) dan LineString (garis/polylines).
- Contoh koordinat (LineString):
[107.4961275, -6.8654203],
[107.4958134, -6.8653953],
[107.4949102, -6.8653158]
- Properties di tiap fitur berisi informasi OSM (OpenStreetMap), misalnya:
{ "@id": "way/306326531", "highway": "service" }
yang menunjukkan bahwa sebagian data berupa jalan (service road).

# Deskripsi GeoJSON Desa

## 📌 Informasi Umum
File ini berisi data spasial dalam format **GeoJSON** yang merepresentasikan titik dan garis pada wilayah desa saya. Data ini diambil/diolah dari OpenStreetMap.

- **Format:** GeoJSON
- **Tipe Utama:** FeatureCollection
- **Jumlah Fitur:** 229
- **Jenis Geometri:** Point dan LineString

## 🗺️ Struktur Data
Setiap fitur dalam file ini memiliki:
- **geometry**: berisi tipe geometrinya (`Point` atau `LineString`) beserta koordinat lintang dan bujur.
- **properties**: berisi atribut tambahan dari data (contoh: jenis jalan, id OSM, dll).

Contoh salah satu fitur:
```json
{
  "type": "Feature",
  "properties": {
    "@id": "way/306326531",
    "highway": "service"
  },
  "geometry": {
    "type": "LineString",
    "coordinates": [
      [107.4961275, -6.8654203],
      [107.4958134, -6.8653953],
      [107.4949102, -6.8653158]
    ]
  }
}

Interpretasi Data

Point merepresentasikan titik penting di wilayah desa (misalnya simpul jalan, lokasi fasilitas, atau titik referensi lain).

LineString merepresentasikan jaringan jalan, jalur, atau batas wilayah.

Koordinat ditulis dalam format longitude, latitude sesuai standar GeoJSON.

💾 Penyimpanan Data

Data GeoJSON ini dapat:

Divisualisasikan di geojson.io

Disimpan dalam MongoDB dengan tipe geospasial (2dsphere)

Digunakan untuk analisis GIS (misalnya query spasial, pencarian lokasi, atau pemetaan rute).

📚 Kesimpulan

File map.geojson berhasil merepresentasikan data spasial desa dengan total 229 fitur berupa titik dan garis. Data ini dapat digunakan untuk visualisasi, analisis spasial, maupun integrasi ke aplikasi berbasis peta.
