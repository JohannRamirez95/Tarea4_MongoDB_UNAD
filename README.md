Microsoft Windows [Versión 10.0.26200.7171]
(c) Microsoft Corporation. Todos los derechos reservados.

C:\Users\johan>mongosh
Current Mongosh Log ID: 691b9af136d8b21a1763b111
Connecting to:          mongodb://127.0.0.1:27017/?directConnection=true&serverSelectionTimeoutMS=2000&appName=mongosh+2.5.9
Using MongoDB:          8.2.1
Using Mongosh:          2.5.9

For mongosh info see: https://www.mongodb.com/docs/mongodb-shell/

------
   The server generated these startup warnings when booting
   2025-11-17T16:41:06.673-05:00: Access control is not enabled for the database. Read and write access to data and configuration is unrestricted
------

test> use dafitiDB
switched to db dafitiDB
dafitiDB> switched to db dafitiDB
Uncaught:
SyntaxError: Missing semicolon. (1:8)

> 1 | switched to db dafitiDB
    |         ^
  2 |

dafitiDB> db.productos.insertMany([
...   { sku: "P001", nombre: "Tenis Running Hombre", categoria: "Calzado", marca: "Adidas", precio: 249900, talla: 42, ccolor: "Negro", stock: 12, vendidos: 58, fechaRegistro: "2025-01-10" },
...   { sku: "P002", nombre: "Camiseta Deportiva Hombre", categoria: "Ropa", marca: "Nike", precio: 89900, talla: "M", color: "Azul", stock: 30, vendidos: 120, fechaRegistro: "2025-02-11" },
...   { sku: "P003", nombre: "Bolso Casual Mujer", categoria: "Accesorios", marca: "Totto", precio: 159900, color: "Rojo", stock: 18, vendidos: 32, fechaRegistro: "2025-03-05" },
...   { sku: "P004", nombre: "Jeans Slim Hombre", categoria: "Ropa", marca: "Levis", precio: 199900, talla: 32, color: "Azul Oscuro", stock: 25, vendidos: 75, fechaRegistro: "2025-04-02" },
...   { sku: "P005", nombre: "Billetera Cuero Hombre", categoria: "Accesorios", marca: "Velez", precio: 129900, color: "Café", stock: 14, vendidos: 41, fechaRegistro: "2025-05-15" },
...   { sku: "P006", nombre: "Sandalias Mujer", categoria: "Calzado", marca: "Studio F", precio: 109900, talla: 37, colocolor: "Blanco", stock: 20, vendidos: 54, fechaRegistro: "2025-06-22" },
...   { sku: "P007", nombre: "Gorra Unisex", categoria: "Accesorios", marca: "Puma", precio: 59900, color: "Negro", stock: 40, vendidos: 150, fechaRegistro: "2025-06-28" },
...   { sku: "P008", nombre: "Chaqueta Impermeable Hombre", categoria: "Ropa", marca: "North Face", precio: 349900, talltalla: "L", color: "Gris", stock: 8, vendidos: 22, fechaRegistro: "2025-07-10" },
...   { sku: "P009", nombre: "Tenis Lifestyle Mujer", categoria: "Calzado", marca: "Nike", precio: 299900, talla: 38, cocolor: "Rosa", stock: 15, vendidos: 66, fechaRegistro: "2025-07-18" },
...   { sku: "P010", nombre: "Camisa Casual Hombre", categoria: "Ropa", marca: "Zara", precio: 119900, talla: "M", color: "Blanca", stock: 10, vendidos: 30, fechaRegistro: "2025-08-01" },
...
...   // 👇 A partir de aquí genero automáticamente P011 – P100
...   ...Array.from({ length: 90 }, (_, i) => {
...     const n = i + 11;
...     return {
...       sku: `P${n.toString().padStart(3, "0")}`,
...       nombre: `Producto ${n}`,
...       categoria: ["Ropa", "Calzado", "Accesorios"][Math.floor(Math.random() * 3)],
...       marca: ["Nike", "Adidas", "Puma", "Velez", "Studio F", "Totto"][Math.floor(Math.random() * 6)],
...       precio: Math.floor(Math.random() * (450000 - 50000) + 50000),
...       talla: ["S", "M", "L", "XL", 36, 38, 40, 42][Math.floor(Math.random() * 8)],
...       color: ["Negro", "Blanco", "Rojo", "Azul", "Gris"][Math.floor(Math.random() * 5)],
...       stock: Math.floor(Math.random() * 50) + 1,
...       vendidos: Math.floor(Math.random() * 200),
...       fechaRegistro: `2025-${String(Math.floor(Math.random() * 12) + 1).padStart(2, "0")}-${String(Math.floor(Math.random() * 28) + 1).padStart(2, "0")}`
...     };
...   })
... ]);
...
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('691b9de636d8b21a1763b112'),
    '1': ObjectId('691b9de636d8b21a1763b113'),
    '2': ObjectId('691b9de636d8b21a1763b114'),
    '3': ObjectId('691b9de636d8b21a1763b115'),
    '4': ObjectId('691b9de636d8b21a1763b116'),
    '5': ObjectId('691b9de636d8b21a1763b117'),
    '6': ObjectId('691b9de636d8b21a1763b118'),
    '7': ObjectId('691b9de636d8b21a1763b119'),
    '8': ObjectId('691b9de636d8b21a1763b11a'),
    '9': ObjectId('691b9de636d8b21a1763b11b'),
    '10': ObjectId('691b9de636d8b21a1763b11c'),
    '11': ObjectId('691b9de636d8b21a1763b11d'),
    '12': ObjectId('691b9de636d8b21a1763b11e'),
    '13': ObjectId('691b9de636d8b21a1763b11f'),
    '14': ObjectId('691b9de636d8b21a1763b120'),
    '15': ObjectId('691b9de636d8b21a1763b121'),
    '16': ObjectId('691b9de636d8b21a1763b122'),
    '17': ObjectId('691b9de636d8b21a1763b123'),
    '18': ObjectId('691b9de636d8b21a1763b124'),
    '19': ObjectId('691b9de636d8b21a1763b125'),
    '20': ObjectId('691b9de636d8b21a1763b126'),
    '21': ObjectId('691b9de636d8b21a1763b127'),
    '22': ObjectId('691b9de636d8b21a1763b128'),
    '23': ObjectId('691b9de636d8b21a1763b129'),
    '24': ObjectId('691b9de636d8b21a1763b12a'),
    '25': ObjectId('691b9de636d8b21a1763b12b'),
    '26': ObjectId('691b9de636d8b21a1763b12c'),
    '27': ObjectId('691b9de636d8b21a1763b12d'),
    '28': ObjectId('691b9de636d8b21a1763b12e'),
    '29': ObjectId('691b9de636d8b21a1763b12f'),
    '30': ObjectId('691b9de636d8b21a1763b130'),
    '31': ObjectId('691b9de636d8b21a1763b131'),
    '32': ObjectId('691b9de636d8b21a1763b132'),
    '33': ObjectId('691b9de636d8b21a1763b133'),
    '34': ObjectId('691b9de636d8b21a1763b134'),
    '35': ObjectId('691b9de636d8b21a1763b135'),
    '36': ObjectId('691b9de636d8b21a1763b136'),
    '37': ObjectId('691b9de636d8b21a1763b137'),
    '38': ObjectId('691b9de636d8b21a1763b138'),
    '39': ObjectId('691b9de636d8b21a1763b139'),
    '40': ObjectId('691b9de636d8b21a1763b13a'),
    '41': ObjectId('691b9de636d8b21a1763b13b'),
    '42': ObjectId('691b9de636d8b21a1763b13c'),
    '43': ObjectId('691b9de636d8b21a1763b13d'),
    '44': ObjectId('691b9de636d8b21a1763b13e'),
    '45': ObjectId('691b9de636d8b21a1763b13f'),
    '46': ObjectId('691b9de636d8b21a1763b140'),
    '47': ObjectId('691b9de636d8b21a1763b141'),
    '48': ObjectId('691b9de636d8b21a1763b142'),
    '49': ObjectId('691b9de636d8b21a1763b143'),
    '50': ObjectId('691b9de636d8b21a1763b144'),
    '51': ObjectId('691b9de636d8b21a1763b145'),
    '52': ObjectId('691b9de636d8b21a1763b146'),
    '53': ObjectId('691b9de636d8b21a1763b147'),
    '54': ObjectId('691b9de636d8b21a1763b148'),
    '55': ObjectId('691b9de636d8b21a1763b149'),
    '56': ObjectId('691b9de636d8b21a1763b14a'),
    '57': ObjectId('691b9de636d8b21a1763b14b'),
    '58': ObjectId('691b9de636d8b21a1763b14c'),
    '59': ObjectId('691b9de636d8b21a1763b14d'),
    '60': ObjectId('691b9de636d8b21a1763b14e'),
    '61': ObjectId('691b9de636d8b21a1763b14f'),
    '62': ObjectId('691b9de636d8b21a1763b150'),
    '63': ObjectId('691b9de636d8b21a1763b151'),
    '64': ObjectId('691b9de636d8b21a1763b152'),
    '65': ObjectId('691b9de636d8b21a1763b153'),
    '66': ObjectId('691b9de636d8b21a1763b154'),
    '67': ObjectId('691b9de636d8b21a1763b155'),
    '68': ObjectId('691b9de636d8b21a1763b156'),
    '69': ObjectId('691b9de636d8b21a1763b157'),
    '70': ObjectId('691b9de636d8b21a1763b158'),
    '71': ObjectId('691b9de636d8b21a1763b159'),
    '72': ObjectId('691b9de636d8b21a1763b15a'),
    '73': ObjectId('691b9de636d8b21a1763b15b'),
    '74': ObjectId('691b9de636d8b21a1763b15c'),
    '75': ObjectId('691b9de636d8b21a1763b15d'),
    '76': ObjectId('691b9de636d8b21a1763b15e'),
    '77': ObjectId('691b9de636d8b21a1763b15f'),
    '78': ObjectId('691b9de636d8b21a1763b160'),
    '79': ObjectId('691b9de636d8b21a1763b161'),
    '80': ObjectId('691b9de636d8b21a1763b162'),
    '81': ObjectId('691b9de636d8b21a1763b163'),
    '82': ObjectId('691b9de636d8b21a1763b164'),
    '83': ObjectId('691b9de636d8b21a1763b165'),
    '84': ObjectId('691b9de636d8b21a1763b166'),
    '85': ObjectId('691b9de636d8b21a1763b167'),
    '86': ObjectId('691b9de636d8b21a1763b168'),
    '87': ObjectId('691b9de636d8b21a1763b169'),
    '88': ObjectId('691b9de636d8b21a1763b16a'),
    '89': ObjectId('691b9de636d8b21a1763b16b'),
    '90': ObjectId('691b9de636d8b21a1763b16c'),
    '91': ObjectId('691b9de636d8b21a1763b16d'),
    '92': ObjectId('691b9de636d8b21a1763b16e'),
    '93': ObjectId('691b9de636d8b21a1763b16f'),
    '94': ObjectId('691b9de636d8b21a1763b170'),
    '95': ObjectId('691b9de636d8b21a1763b171'),
    '96': ObjectId('691b9de636d8b21a1763b172'),
    '97': ObjectId('691b9de636d8b21a1763b173'),
    '98': ObjectId('691b9de636d8b21a1763b174'),
    '99': ObjectId('691b9de636d8b21a1763b175')
  }
}
dafitiDB> db.productos.countDocuments()
100
dafitiDB> db.productos.findOne()
{
  _id: ObjectId('691b9de636d8b21a1763b112'),
  sku: 'P001',
  nombre: 'Tenis Running Hombre',
  categoria: 'Calzado',
  marca: 'Adidas',
  precio: 249900,
  talla: 42,
  color: 'Negro',
  stock: 12,
  vendidos: 58,
  fechaRegistro: '2025-01-10'
}
dafitiDB> db.productos.find()
[
  {
    _id: ObjectId('691b9de636d8b21a1763b112'),
    sku: 'P001',
    nombre: 'Tenis Running Hombre',
    categoria: 'Calzado',
    marca: 'Adidas',
    precio: 249900,
    talla: 42,
    color: 'Negro',
    stock: 12,
    vendidos: 58,
    fechaRegistro: '2025-01-10'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b113'),
    sku: 'P002',
    nombre: 'Camiseta Deportiva Hombre',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 89900,
    talla: 'M',
    color: 'Azul',
    stock: 30,
    vendidos: 120,
    fechaRegistro: '2025-02-11'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b114'),
    sku: 'P003',
    nombre: 'Bolso Casual Mujer',
    categoria: 'Accesorios',
    marca: 'Totto',
    precio: 159900,
    color: 'Rojo',
    stock: 18,
    vendidos: 32,
    fechaRegistro: '2025-03-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b115'),
    sku: 'P004',
    nombre: 'Jeans Slim Hombre',
    categoria: 'Ropa',
    marca: 'Levis',
    precio: 199900,
    talla: 32,
    color: 'Azul Oscuro',
    stock: 25,
    vendidos: 75,
    fechaRegistro: '2025-04-02'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b116'),
    sku: 'P005',
    nombre: 'Billetera Cuero Hombre',
    categoria: 'Accesorios',
    marca: 'Velez',
    precio: 129900,
    color: 'Café',
    stock: 14,
    vendidos: 41,
    fechaRegistro: '2025-05-15'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b117'),
    sku: 'P006',
    nombre: 'Sandalias Mujer',
    categoria: 'Calzado',
    marca: 'Studio F',
    precio: 109900,
    talla: 37,
    color: 'Blanco',
    stock: 20,
    vendidos: 54,
    fechaRegistro: '2025-06-22'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b118'),
    sku: 'P007',
    nombre: 'Gorra Unisex',
    categoria: 'Accesorios',
    marca: 'Puma',
    precio: 59900,
    color: 'Negro',
    stock: 40,
    vendidos: 150,
    fechaRegistro: '2025-06-28'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b119'),
    sku: 'P008',
    nombre: 'Chaqueta Impermeable Hombre',
    categoria: 'Ropa',
    marca: 'North Face',
    precio: 349900,
    talla: 'L',
    color: 'Gris',
    stock: 8,
    vendidos: 22,
    fechaRegistro: '2025-07-10'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11a'),
    sku: 'P009',
    nombre: 'Tenis Lifestyle Mujer',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 299900,
    talla: 38,
    color: 'Rosa',
    stock: 15,
    vendidos: 66,
    fechaRegistro: '2025-07-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11b'),
    sku: 'P010',
    nombre: 'Camisa Casual Hombre',
    categoria: 'Ropa',
    marca: 'Zara',
    precio: 119900,
    talla: 'M',
    color: 'Blanca',
    stock: 10,
    vendidos: 30,
    fechaRegistro: '2025-08-01'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11c'),
    sku: 'P011',
    nombre: 'Producto 11',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 418220,
    talla: 42,
    color: 'Negro',
    stock: 49,
    vendidos: 32,
    fechaRegistro: '2025-11-12'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11d'),
    sku: 'P012',
    nombre: 'Producto 12',
    categoria: 'Calzado',
    marca: 'Totto',
    precio: 279025,
    talla: 'XL',
    color: 'Rojo',
    stock: 20,
    vendidos: 144,
    fechaRegistro: '2025-07-08'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11e'),
    sku: 'P013',
    nombre: 'Producto 13',
    categoria: 'Ropa',
    marca: 'Adidas',
    precio: 125351,
    talla: 38,
    color: 'Azul',
    stock: 37,
    vendidos: 41,
    fechaRegistro: '2025-04-25'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11f'),
    sku: 'P014',
    nombre: 'Producto 14',
    categoria: 'Accesorios',
    marca: 'Adidas',
    precio: 176127,
    talla: 42,
    color: 'Rojo',
    stock: 32,
    vendidos: 27,
    fechaRegistro: '2025-04-09'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b120'),
    sku: 'P015',
    nombre: 'Producto 15',
    categoria: 'Calzado',
    marca: 'Totto',
    precio: 410111,
    talla: 'XL',
    color: 'Negro',
    stock: 15,
    vendidos: 63,
    fechaRegistro: '2025-09-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b121'),
    sku: 'P016',
    nombre: 'Producto 16',
    categoria: 'Accesorios',
    marca: 'Puma',
    precio: 322919,
    talla: 'S',
    color: 'Blanco',
    stock: 15,
    vendidos: 61,
    fechaRegistro: '2025-01-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b122'),
    sku: 'P017',
    nombre: 'Producto 17',
    categoria: 'Accesorios',
    marca: 'Velez',
    precio: 404512,
    talla: 'M',
    color: 'Blanco',
    stock: 33,
    vendidos: 175,
    fechaRegistro: '2025-05-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b123'),
    sku: 'P018',
    nombre: 'Producto 18',
    categoria: 'Accesorios',
    marca: 'Velez',
    precio: 131491,
    talla: 'M',
    color: 'Blanco',
    stock: 7,
    vendidos: 144,
    fechaRegistro: '2025-07-21'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b124'),
    sku: 'P019',
    nombre: 'Producto 19',
    categoria: 'Accesorios',
    marca: 'Adidas',
    precio: 76646,
    talla: 'M',
    color: 'Negro',
    stock: 18,
    vendidos: 113,
    fechaRegistro: '2025-11-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b125'),
    sku: 'P020',
    nombre: 'Producto 20',
    categoria: 'Accesorios',
    marca: 'Studio F',
    precio: 355348,
    talla: 40,
    color: 'Rojo',
    stock: 20,
    vendidos: 66,
    fechaRegistro: '2025-05-09'
  }
]
Type "it" for more
dafitiDB> db.productos.countDocuments()
100
dafitiDB> db.productos.insertOne({
...   sku: "PX001",
...   nombre: "Bolso Casual Mujer",
...   categoria: "Accesorios",
...   marca: "Totto",
...   precio: 159900,
...   talla: null,
...   color: "Rojo",
...   stock: 20,
...   vendidos: 5,
...   fechaRegistro: "2025-02-01"
... })
...
{
  acknowledged: true,
  insertedId: ObjectId('691ba02b36d8b21a1763b176')
}
dafitiDB> db.productos.updateOne(
...   { sku: "PX001" },
...   { $set: { precio: 179900 } }
... )
...
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
dafitiDB> db.productos.deleteOne({ sku: "PX001" })
{ acknowledged: true, deletedCount: 1 }
dafitiDB> db.productos.find({ categoria: "Calzado" })
[
  {
    _id: ObjectId('691b9de636d8b21a1763b112'),
    sku: 'P001',
    nombre: 'Tenis Running Hombre',
    categoria: 'Calzado',
    marca: 'Adidas',
    precio: 249900,
    talla: 42,
    color: 'Negro',
    stock: 12,
    vendidos: 58,
    fechaRegistro: '2025-01-10'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b117'),
    sku: 'P006',
    nombre: 'Sandalias Mujer',
    categoria: 'Calzado',
    marca: 'Studio F',
    precio: 109900,
    talla: 37,
    color: 'Blanco',
    stock: 20,
    vendidos: 54,
    fechaRegistro: '2025-06-22'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11a'),
    sku: 'P009',
    nombre: 'Tenis Lifestyle Mujer',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 299900,
    talla: 38,
    color: 'Rosa',
    stock: 15,
    vendidos: 66,
    fechaRegistro: '2025-07-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11d'),
    sku: 'P012',
    nombre: 'Producto 12',
    categoria: 'Calzado',
    marca: 'Totto',
    precio: 279025,
    talla: 'XL',
    color: 'Rojo',
    stock: 20,
    vendidos: 144,
    fechaRegistro: '2025-07-08'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b120'),
    sku: 'P015',
    nombre: 'Producto 15',
    categoria: 'Calzado',
    marca: 'Totto',
    precio: 410111,
    talla: 'XL',
    color: 'Negro',
    stock: 15,
    vendidos: 63,
    fechaRegistro: '2025-09-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b126'),
    sku: 'P021',
    nombre: 'Producto 21',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 385201,
    talla: 42,
    color: 'Blanco',
    stock: 14,
    vendidos: 199,
    fechaRegistro: '2025-06-12'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12a'),
    sku: 'P025',
    nombre: 'Producto 25',
    categoria: 'Calzado',
    marca: 'Velez',
    precio: 201258,
    talla: 'L',
    color: 'Rojo',
    stock: 4,
    vendidos: 135,
    fechaRegistro: '2025-12-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12e'),
    sku: 'P029',
    nombre: 'Producto 29',
    categoria: 'Calzado',
    marca: 'Puma',
    precio: 112194,
    talla: 40,
    color: 'Azul',
    stock: 12,
    vendidos: 21,
    fechaRegistro: '2025-10-01'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12f'),
    sku: 'P030',
    nombre: 'Producto 30',
    categoria: 'Calzado',
    marca: 'Adidas',
    precio: 434153,
    talla: 40,
    color: 'Rojo',
    stock: 8,
    vendidos: 122,
    fechaRegistro: '2025-01-23'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b138'),
    sku: 'P039',
    nombre: 'Producto 39',
    categoria: 'Calzado',
    marca: 'Puma',
    precio: 101439,
    talla: 'XL',
    color: 'Rojo',
    stock: 43,
    vendidos: 48,
    fechaRegistro: '2025-11-06'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b145'),
    sku: 'P052',
    nombre: 'Producto 52',
    categoria: 'Calzado',
    marca: 'Velez',
    precio: 151991,
    talla: 'S',
    color: 'Blanco',
    stock: 3,
    vendidos: 74,
    fechaRegistro: '2025-09-21'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b147'),
    sku: 'P054',
    nombre: 'Producto 54',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 291397,
    talla: 'S',
    color: 'Negro',
    stock: 50,
    vendidos: 191,
    fechaRegistro: '2025-06-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b148'),
    sku: 'P055',
    nombre: 'Producto 55',
    categoria: 'Calzado',
    marca: 'Puma',
    precio: 435250,
    talla: 40,
    color: 'Rojo',
    stock: 16,
    vendidos: 6,
    fechaRegistro: '2025-06-01'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b14c'),
    sku: 'P059',
    nombre: 'Producto 59',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 321199,
    talla: 38,
    color: 'Azul',
    stock: 32,
    vendidos: 192,
    fechaRegistro: '2025-12-19'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b14f'),
    sku: 'P062',
    nombre: 'Producto 62',
    categoria: 'Calzado',
    marca: 'Velez',
    precio: 299167,
    talla: 'L',
    color: 'Blanco',
    stock: 7,
    vendidos: 0,
    fechaRegistro: '2025-02-26'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b151'),
    sku: 'P064',
    nombre: 'Producto 64',
    categoria: 'Calzado',
    marca: 'Studio F',
    precio: 263367,
    talla: 'XL',
    color: 'Blanco',
    stock: 39,
    vendidos: 61,
    fechaRegistro: '2025-12-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b158'),
    sku: 'P071',
    nombre: 'Producto 71',
    categoria: 'Calzado',
    marca: 'Studio F',
    precio: 251550,
    talla: 42,
    color: 'Gris',
    stock: 22,
    vendidos: 131,
    fechaRegistro: '2025-04-01'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b159'),
    sku: 'P072',
    nombre: 'Producto 72',
    categoria: 'Calzado',
    marca: 'Studio F',
    precio: 255697,
    talla: 40,
    color: 'Azul',
    stock: 18,
    vendidos: 115,
    fechaRegistro: '2025-01-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b15b'),
    sku: 'P074',
    nombre: 'Producto 74',
    categoria: 'Calzado',
    marca: 'Puma',
    precio: 295350,
    talla: 'L',
    color: 'Gris',
    stock: 29,
    vendidos: 161,
    fechaRegistro: '2025-12-13'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b15d'),
    sku: 'P076',
    nombre: 'Producto 76',
    categoria: 'Calzado',
    marca: 'Puma',
    precio: 350320,
    talla: 'S',
    color: 'Gris',
    stock: 23,
    vendidos: 38,
    fechaRegistro: '2025-08-25'
  }
]
Type "it" for more
dafitiDB> db.productos.find({ marca: "Nike" })
[
  {
    _id: ObjectId('691b9de636d8b21a1763b113'),
    sku: 'P002',
    nombre: 'Camiseta Deportiva Hombre',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 89900,
    talla: 'M',
    color: 'Azul',
    stock: 30,
    vendidos: 120,
    fechaRegistro: '2025-02-11'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11a'),
    sku: 'P009',
    nombre: 'Tenis Lifestyle Mujer',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 299900,
    talla: 38,
    color: 'Rosa',
    stock: 15,
    vendidos: 66,
    fechaRegistro: '2025-07-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11c'),
    sku: 'P011',
    nombre: 'Producto 11',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 418220,
    talla: 42,
    color: 'Negro',
    stock: 49,
    vendidos: 32,
    fechaRegistro: '2025-11-12'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b126'),
    sku: 'P021',
    nombre: 'Producto 21',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 385201,
    talla: 42,
    color: 'Blanco',
    stock: 14,
    vendidos: 199,
    fechaRegistro: '2025-06-12'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12d'),
    sku: 'P028',
    nombre: 'Producto 28',
    categoria: 'Accesorios',
    marca: 'Nike',
    precio: 427237,
    talla: 38,
    color: 'Azul',
    stock: 28,
    vendidos: 55,
    fechaRegistro: '2025-04-12'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b131'),
    sku: 'P032',
    nombre: 'Producto 32',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 432742,
    talla: 'L',
    color: 'Negro',
    stock: 43,
    vendidos: 32,
    fechaRegistro: '2025-10-28'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b134'),
    sku: 'P035',
    nombre: 'Producto 35',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 140793,
    talla: 'L',
    color: 'Gris',
    stock: 9,
    vendidos: 50,
    fechaRegistro: '2025-12-20'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b135'),
    sku: 'P036',
    nombre: 'Producto 36',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 449999,
    talla: 'XL',
    color: 'Rojo',
    stock: 43,
    vendidos: 41,
    fechaRegistro: '2025-11-27'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b137'),
    sku: 'P038',
    nombre: 'Producto 38',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 448863,
    talla: 42,
    color: 'Azul',
    stock: 22,
    vendidos: 11,
    fechaRegistro: '2025-05-06'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b13d'),
    sku: 'P044',
    nombre: 'Producto 44',
    categoria: 'Accesorios',
    marca: 'Nike',
    precio: 206373,
    talla: 42,
    color: 'Negro',
    stock: 4,
    vendidos: 108,
    fechaRegistro: '2025-02-10'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b143'),
    sku: 'P050',
    nombre: 'Producto 50',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 66337,
    talla: 'XL',
    color: 'Negro',
    stock: 4,
    vendidos: 11,
    fechaRegistro: '2025-04-23'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b147'),
    sku: 'P054',
    nombre: 'Producto 54',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 291397,
    talla: 'S',
    color: 'Negro',
    stock: 50,
    vendidos: 191,
    fechaRegistro: '2025-06-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b14c'),
    sku: 'P059',
    nombre: 'Producto 59',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 321199,
    talla: 38,
    color: 'Azul',
    stock: 32,
    vendidos: 192,
    fechaRegistro: '2025-12-19'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b14e'),
    sku: 'P061',
    nombre: 'Producto 61',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 294821,
    talla: 42,
    color: 'Gris',
    stock: 19,
    vendidos: 173,
    fechaRegistro: '2025-01-17'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b152'),
    sku: 'P065',
    nombre: 'Producto 65',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 224584,
    talla: 'L',
    color: 'Blanco',
    stock: 21,
    vendidos: 78,
    fechaRegistro: '2025-03-26'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b155'),
    sku: 'P068',
    nombre: 'Producto 68',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 299696,
    talla: 36,
    color: 'Gris',
    stock: 46,
    vendidos: 104,
    fechaRegistro: '2025-02-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b15a'),
    sku: 'P073',
    nombre: 'Producto 73',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 144877,
    talla: 'XL',
    color: 'Negro',
    stock: 17,
    vendidos: 84,
    fechaRegistro: '2025-06-09'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b15c'),
    sku: 'P075',
    nombre: 'Producto 75',
    categoria: 'Accesorios',
    marca: 'Nike',
    precio: 162951,
    talla: 'L',
    color: 'Rojo',
    stock: 9,
    vendidos: 3,
    fechaRegistro: '2025-08-07'
  }
]
dafitiDB> db.productos.find({ precio: { $gt: 200000 } })
[
  {
    _id: ObjectId('691b9de636d8b21a1763b112'),
    sku: 'P001',
    nombre: 'Tenis Running Hombre',
    categoria: 'Calzado',
    marca: 'Adidas',
    precio: 249900,
    talla: 42,
    color: 'Negro',
    stock: 12,
    vendidos: 58,
    fechaRegistro: '2025-01-10'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b119'),
    sku: 'P008',
    nombre: 'Chaqueta Impermeable Hombre',
    categoria: 'Ropa',
    marca: 'North Face',
    precio: 349900,
    talla: 'L',
    color: 'Gris',
    stock: 8,
    vendidos: 22,
    fechaRegistro: '2025-07-10'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11a'),
    sku: 'P009',
    nombre: 'Tenis Lifestyle Mujer',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 299900,
    talla: 38,
    color: 'Rosa',
    stock: 15,
    vendidos: 66,
    fechaRegistro: '2025-07-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11c'),
    sku: 'P011',
    nombre: 'Producto 11',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 418220,
    talla: 42,
    color: 'Negro',
    stock: 49,
    vendidos: 32,
    fechaRegistro: '2025-11-12'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11d'),
    sku: 'P012',
    nombre: 'Producto 12',
    categoria: 'Calzado',
    marca: 'Totto',
    precio: 279025,
    talla: 'XL',
    color: 'Rojo',
    stock: 20,
    vendidos: 144,
    fechaRegistro: '2025-07-08'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b120'),
    sku: 'P015',
    nombre: 'Producto 15',
    categoria: 'Calzado',
    marca: 'Totto',
    precio: 410111,
    talla: 'XL',
    color: 'Negro',
    stock: 15,
    vendidos: 63,
    fechaRegistro: '2025-09-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b121'),
    sku: 'P016',
    nombre: 'Producto 16',
    categoria: 'Accesorios',
    marca: 'Puma',
    precio: 322919,
    talla: 'S',
    color: 'Blanco',
    stock: 15,
    vendidos: 61,
    fechaRegistro: '2025-01-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b122'),
    sku: 'P017',
    nombre: 'Producto 17',
    categoria: 'Accesorios',
    marca: 'Velez',
    precio: 404512,
    talla: 'M',
    color: 'Blanco',
    stock: 33,
    vendidos: 175,
    fechaRegistro: '2025-05-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b125'),
    sku: 'P020',
    nombre: 'Producto 20',
    categoria: 'Accesorios',
    marca: 'Studio F',
    precio: 355348,
    talla: 40,
    color: 'Rojo',
    stock: 20,
    vendidos: 66,
    fechaRegistro: '2025-05-09'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b126'),
    sku: 'P021',
    nombre: 'Producto 21',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 385201,
    talla: 42,
    color: 'Blanco',
    stock: 14,
    vendidos: 199,
    fechaRegistro: '2025-06-12'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b127'),
    sku: 'P022',
    nombre: 'Producto 22',
    categoria: 'Accesorios',
    marca: 'Totto',
    precio: 416333,
    talla: 'M',
    color: 'Rojo',
    stock: 11,
    vendidos: 18,
    fechaRegistro: '2025-02-13'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b128'),
    sku: 'P023',
    nombre: 'Producto 23',
    categoria: 'Ropa',
    marca: 'Velez',
    precio: 274325,
    talla: 40,
    color: 'Blanco',
    stock: 23,
    vendidos: 180,
    fechaRegistro: '2025-06-28'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b129'),
    sku: 'P024',
    nombre: 'Producto 24',
    categoria: 'Accesorios',
    marca: 'Totto',
    precio: 272639,
    talla: 36,
    color: 'Blanco',
    stock: 28,
    vendidos: 133,
    fechaRegistro: '2025-10-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12a'),
    sku: 'P025',
    nombre: 'Producto 25',
    categoria: 'Calzado',
    marca: 'Velez',
    precio: 201258,
    talla: 'L',
    color: 'Rojo',
    stock: 4,
    vendidos: 135,
    fechaRegistro: '2025-12-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12b'),
    sku: 'P026',
    nombre: 'Producto 26',
    categoria: 'Accesorios',
    marca: 'Adidas',
    precio: 446233,
    talla: 'L',
    color: 'Azul',
    stock: 43,
    vendidos: 93,
    fechaRegistro: '2025-01-17'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12d'),
    sku: 'P028',
    nombre: 'Producto 28',
    categoria: 'Accesorios',
    marca: 'Nike',
    precio: 427237,
    talla: 38,
    color: 'Azul',
    stock: 28,
    vendidos: 55,
    fechaRegistro: '2025-04-12'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12f'),
    sku: 'P030',
    nombre: 'Producto 30',
    categoria: 'Calzado',
    marca: 'Adidas',
    precio: 434153,
    talla: 40,
    color: 'Rojo',
    stock: 8,
    vendidos: 122,
    fechaRegistro: '2025-01-23'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b131'),
    sku: 'P032',
    nombre: 'Producto 32',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 432742,
    talla: 'L',
    color: 'Negro',
    stock: 43,
    vendidos: 32,
    fechaRegistro: '2025-10-28'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b135'),
    sku: 'P036',
    nombre: 'Producto 36',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 449999,
    talla: 'XL',
    color: 'Rojo',
    stock: 43,
    vendidos: 41,
    fechaRegistro: '2025-11-27'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b137'),
    sku: 'P038',
    nombre: 'Producto 38',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 448863,
    talla: 42,
    color: 'Azul',
    stock: 22,
    vendidos: 11,
    fechaRegistro: '2025-05-06'
  }
]
Type "it" for more
dafitiDB> db.productos.find({
...   precio: { $gte: 100000, $lte: 300000 }
... })
...
[
  {
    _id: ObjectId('691b9de636d8b21a1763b112'),
    sku: 'P001',
    nombre: 'Tenis Running Hombre',
    categoria: 'Calzado',
    marca: 'Adidas',
    precio: 249900,
    talla: 42,
    color: 'Negro',
    stock: 12,
    vendidos: 58,
    fechaRegistro: '2025-01-10'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b114'),
    sku: 'P003',
    nombre: 'Bolso Casual Mujer',
    categoria: 'Accesorios',
    marca: 'Totto',
    precio: 159900,
    color: 'Rojo',
    stock: 18,
    vendidos: 32,
    fechaRegistro: '2025-03-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b115'),
    sku: 'P004',
    nombre: 'Jeans Slim Hombre',
    categoria: 'Ropa',
    marca: 'Levis',
    precio: 199900,
    talla: 32,
    color: 'Azul Oscuro',
    stock: 25,
    vendidos: 75,
    fechaRegistro: '2025-04-02'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b116'),
    sku: 'P005',
    nombre: 'Billetera Cuero Hombre',
    categoria: 'Accesorios',
    marca: 'Velez',
    precio: 129900,
    color: 'Café',
    stock: 14,
    vendidos: 41,
    fechaRegistro: '2025-05-15'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b117'),
    sku: 'P006',
    nombre: 'Sandalias Mujer',
    categoria: 'Calzado',
    marca: 'Studio F',
    precio: 109900,
    talla: 37,
    color: 'Blanco',
    stock: 20,
    vendidos: 54,
    fechaRegistro: '2025-06-22'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11a'),
    sku: 'P009',
    nombre: 'Tenis Lifestyle Mujer',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 299900,
    talla: 38,
    color: 'Rosa',
    stock: 15,
    vendidos: 66,
    fechaRegistro: '2025-07-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11b'),
    sku: 'P010',
    nombre: 'Camisa Casual Hombre',
    categoria: 'Ropa',
    marca: 'Zara',
    precio: 119900,
    talla: 'M',
    color: 'Blanca',
    stock: 10,
    vendidos: 30,
    fechaRegistro: '2025-08-01'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11d'),
    sku: 'P012',
    nombre: 'Producto 12',
    categoria: 'Calzado',
    marca: 'Totto',
    precio: 279025,
    talla: 'XL',
    color: 'Rojo',
    stock: 20,
    vendidos: 144,
    fechaRegistro: '2025-07-08'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11e'),
    sku: 'P013',
    nombre: 'Producto 13',
    categoria: 'Ropa',
    marca: 'Adidas',
    precio: 125351,
    talla: 38,
    color: 'Azul',
    stock: 37,
    vendidos: 41,
    fechaRegistro: '2025-04-25'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11f'),
    sku: 'P014',
    nombre: 'Producto 14',
    categoria: 'Accesorios',
    marca: 'Adidas',
    precio: 176127,
    talla: 42,
    color: 'Rojo',
    stock: 32,
    vendidos: 27,
    fechaRegistro: '2025-04-09'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b123'),
    sku: 'P018',
    nombre: 'Producto 18',
    categoria: 'Accesorios',
    marca: 'Velez',
    precio: 131491,
    talla: 'M',
    color: 'Blanco',
    stock: 7,
    vendidos: 144,
    fechaRegistro: '2025-07-21'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b128'),
    sku: 'P023',
    nombre: 'Producto 23',
    categoria: 'Ropa',
    marca: 'Velez',
    precio: 274325,
    talla: 40,
    color: 'Blanco',
    stock: 23,
    vendidos: 180,
    fechaRegistro: '2025-06-28'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b129'),
    sku: 'P024',
    nombre: 'Producto 24',
    categoria: 'Accesorios',
    marca: 'Totto',
    precio: 272639,
    talla: 36,
    color: 'Blanco',
    stock: 28,
    vendidos: 133,
    fechaRegistro: '2025-10-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12a'),
    sku: 'P025',
    nombre: 'Producto 25',
    categoria: 'Calzado',
    marca: 'Velez',
    precio: 201258,
    talla: 'L',
    color: 'Rojo',
    stock: 4,
    vendidos: 135,
    fechaRegistro: '2025-12-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12c'),
    sku: 'P027',
    nombre: 'Producto 27',
    categoria: 'Accesorios',
    marca: 'Puma',
    precio: 158910,
    talla: 38,
    color: 'Azul',
    stock: 40,
    vendidos: 121,
    fechaRegistro: '2025-06-16'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12e'),
    sku: 'P029',
    nombre: 'Producto 29',
    categoria: 'Calzado',
    marca: 'Puma',
    precio: 112194,
    talla: 40,
    color: 'Azul',
    stock: 12,
    vendidos: 21,
    fechaRegistro: '2025-10-01'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b134'),
    sku: 'P035',
    nombre: 'Producto 35',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 140793,
    talla: 'L',
    color: 'Gris',
    stock: 9,
    vendidos: 50,
    fechaRegistro: '2025-12-20'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b138'),
    sku: 'P039',
    nombre: 'Producto 39',
    categoria: 'Calzado',
    marca: 'Puma',
    precio: 101439,
    talla: 'XL',
    color: 'Rojo',
    stock: 43,
    vendidos: 48,
    fechaRegistro: '2025-11-06'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b139'),
    sku: 'P040',
    nombre: 'Producto 40',
    categoria: 'Accesorios',
    marca: 'Totto',
    precio: 113257,
    talla: 36,
    color: 'Rojo',
    stock: 49,
    vendidos: 106,
    fechaRegistro: '2025-10-16'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b13b'),
    sku: 'P042',
    nombre: 'Producto 42',
    categoria: 'Ropa',
    marca: 'Totto',
    precio: 110541,
    talla: 'S',
    color: 'Gris',
    stock: 6,
    vendidos: 179,
    fechaRegistro: '2025-01-06'
  }
]
Type "it" for more
dafitiDB> db.productos.find({ stock: { $lt: 5 } })
[
  {
    _id: ObjectId('691b9de636d8b21a1763b12a'),
    sku: 'P025',
    nombre: 'Producto 25',
    categoria: 'Calzado',
    marca: 'Velez',
    precio: 201258,
    talla: 'L',
    color: 'Rojo',
    stock: 4,
    vendidos: 135,
    fechaRegistro: '2025-12-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b132'),
    sku: 'P033',
    nombre: 'Producto 33',
    categoria: 'Ropa',
    marca: 'Velez',
    precio: 64919,
    talla: 'XL',
    color: 'Negro',
    stock: 4,
    vendidos: 41,
    fechaRegistro: '2025-03-03'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b13d'),
    sku: 'P044',
    nombre: 'Producto 44',
    categoria: 'Accesorios',
    marca: 'Nike',
    precio: 206373,
    talla: 42,
    color: 'Negro',
    stock: 4,
    vendidos: 108,
    fechaRegistro: '2025-02-10'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b141'),
    sku: 'P048',
    nombre: 'Producto 48',
    categoria: 'Ropa',
    marca: 'Studio F',
    precio: 364307,
    talla: 'S',
    color: 'Azul',
    stock: 4,
    vendidos: 193,
    fechaRegistro: '2025-05-21'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b143'),
    sku: 'P050',
    nombre: 'Producto 50',
    categoria: 'Ropa',
    marca: 'Nike',
    precio: 66337,
    talla: 'XL',
    color: 'Negro',
    stock: 4,
    vendidos: 11,
    fechaRegistro: '2025-04-23'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b145'),
    sku: 'P052',
    nombre: 'Producto 52',
    categoria: 'Calzado',
    marca: 'Velez',
    precio: 151991,
    talla: 'S',
    color: 'Blanco',
    stock: 3,
    vendidos: 74,
    fechaRegistro: '2025-09-21'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b156'),
    sku: 'P069',
    nombre: 'Producto 69',
    categoria: 'Ropa',
    marca: 'Totto',
    precio: 69615,
    talla: 'L',
    color: 'Gris',
    stock: 4,
    vendidos: 171,
    fechaRegistro: '2025-06-16'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b162'),
    sku: 'P081',
    nombre: 'Producto 81',
    categoria: 'Ropa',
    marca: 'Adidas',
    precio: 187085,
    talla: 'S',
    color: 'Azul',
    stock: 2,
    vendidos: 170,
    fechaRegistro: '2025-03-12'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b164'),
    sku: 'P083',
    nombre: 'Producto 83',
    categoria: 'Ropa',
    marca: 'Adidas',
    precio: 297981,
    talla: 'S',
    color: 'Azul',
    stock: 2,
    vendidos: 135,
    fechaRegistro: '2025-10-18'
  }
]
dafitiDB> db.productos.find({
...   $and: [
...     { color: "Negro" },
...     { categoria: "Calzado" }
...   ]
... })
...
[
  {
    _id: ObjectId('691b9de636d8b21a1763b112'),
    sku: 'P001',
    nombre: 'Tenis Running Hombre',
    categoria: 'Calzado',
    marca: 'Adidas',
    precio: 249900,
    talla: 42,
    color: 'Negro',
    stock: 12,
    vendidos: 58,
    fechaRegistro: '2025-01-10'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b120'),
    sku: 'P015',
    nombre: 'Producto 15',
    categoria: 'Calzado',
    marca: 'Totto',
    precio: 410111,
    talla: 'XL',
    color: 'Negro',
    stock: 15,
    vendidos: 63,
    fechaRegistro: '2025-09-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b147'),
    sku: 'P054',
    nombre: 'Producto 54',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 291397,
    talla: 'S',
    color: 'Negro',
    stock: 50,
    vendidos: 191,
    fechaRegistro: '2025-06-05'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b160'),
    sku: 'P079',
    nombre: 'Producto 79',
    categoria: 'Calzado',
    marca: 'Velez',
    precio: 89495,
    talla: 38,
    color: 'Negro',
    stock: 34,
    vendidos: 95,
    fechaRegistro: '2025-10-13'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b172'),
    sku: 'P097',
    nombre: 'Producto 97',
    categoria: 'Calzado',
    marca: 'Puma',
    precio: 290553,
    talla: 40,
    color: 'Negro',
    stock: 39,
    vendidos: 137,
    fechaRegistro: '2025-03-16'
  }
]
dafitiDB> db.productos.find({
...   $or: [
...     { marca: "Adidas" },
...     { marca: "Puma" }
...   ]
... })
...
[
  {
    _id: ObjectId('691b9de636d8b21a1763b112'),
    sku: 'P001',
    nombre: 'Tenis Running Hombre',
    categoria: 'Calzado',
    marca: 'Adidas',
    precio: 249900,
    talla: 42,
    color: 'Negro',
    stock: 12,
    vendidos: 58,
    fechaRegistro: '2025-01-10'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b118'),
    sku: 'P007',
    nombre: 'Gorra Unisex',
    categoria: 'Accesorios',
    marca: 'Puma',
    precio: 59900,
    color: 'Negro',
    stock: 40,
    vendidos: 150,
    fechaRegistro: '2025-06-28'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11e'),
    sku: 'P013',
    nombre: 'Producto 13',
    categoria: 'Ropa',
    marca: 'Adidas',
    precio: 125351,
    talla: 38,
    color: 'Azul',
    stock: 37,
    vendidos: 41,
    fechaRegistro: '2025-04-25'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11f'),
    sku: 'P014',
    nombre: 'Producto 14',
    categoria: 'Accesorios',
    marca: 'Adidas',
    precio: 176127,
    talla: 42,
    color: 'Rojo',
    stock: 32,
    vendidos: 27,
    fechaRegistro: '2025-04-09'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b121'),
    sku: 'P016',
    nombre: 'Producto 16',
    categoria: 'Accesorios',
    marca: 'Puma',
    precio: 322919,
    talla: 'S',
    color: 'Blanco',
    stock: 15,
    vendidos: 61,
    fechaRegistro: '2025-01-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b124'),
    sku: 'P019',
    nombre: 'Producto 19',
    categoria: 'Accesorios',
    marca: 'Adidas',
    precio: 76646,
    talla: 'M',
    color: 'Negro',
    stock: 18,
    vendidos: 113,
    fechaRegistro: '2025-11-18'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12b'),
    sku: 'P026',
    nombre: 'Producto 26',
    categoria: 'Accesorios',
    marca: 'Adidas',
    precio: 446233,
    talla: 'L',
    color: 'Azul',
    stock: 43,
    vendidos: 93,
    fechaRegistro: '2025-01-17'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12c'),
    sku: 'P027',
    nombre: 'Producto 27',
    categoria: 'Accesorios',
    marca: 'Puma',
    precio: 158910,
    talla: 38,
    color: 'Azul',
    stock: 40,
    vendidos: 121,
    fechaRegistro: '2025-06-16'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12e'),
    sku: 'P029',
    nombre: 'Producto 29',
    categoria: 'Calzado',
    marca: 'Puma',
    precio: 112194,
    talla: 40,
    color: 'Azul',
    stock: 12,
    vendidos: 21,
    fechaRegistro: '2025-10-01'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b12f'),
    sku: 'P030',
    nombre: 'Producto 30',
    categoria: 'Calzado',
    marca: 'Adidas',
    precio: 434153,
    talla: 40,
    color: 'Rojo',
    stock: 8,
    vendidos: 122,
    fechaRegistro: '2025-01-23'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b130'),
    sku: 'P031',
    nombre: 'Producto 31',
    categoria: 'Accesorios',
    marca: 'Puma',
    precio: 67565,
    talla: 'L',
    color: 'Negro',
    stock: 50,
    vendidos: 56,
    fechaRegistro: '2025-03-09'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b138'),
    sku: 'P039',
    nombre: 'Producto 39',
    categoria: 'Calzado',
    marca: 'Puma',
    precio: 101439,
    talla: 'XL',
    color: 'Rojo',
    stock: 43,
    vendidos: 48,
    fechaRegistro: '2025-11-06'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b148'),
    sku: 'P055',
    nombre: 'Producto 55',
    categoria: 'Calzado',
    marca: 'Puma',
    precio: 435250,
    talla: 40,
    color: 'Rojo',
    stock: 16,
    vendidos: 6,
    fechaRegistro: '2025-06-01'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b14a'),
    sku: 'P057',
    nombre: 'Producto 57',
    categoria: 'Ropa',
    marca: 'Adidas',
    precio: 279771,
    talla: 40,
    color: 'Negro',
    stock: 36,
    vendidos: 157,
    fechaRegistro: '2025-11-16'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b14b'),
    sku: 'P058',
    nombre: 'Producto 58',
    categoria: 'Accesorios',
    marca: 'Puma',
    precio: 129833,
    talla: 42,
    color: 'Azul',
    stock: 33,
    vendidos: 22,
    fechaRegistro: '2025-12-03'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b150'),
    sku: 'P063',
    nombre: 'Producto 63',
    categoria: 'Ropa',
    marca: 'Adidas',
    precio: 302588,
    talla: 42,
    color: 'Negro',
    stock: 28,
    vendidos: 19,
    fechaRegistro: '2025-10-19'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b157'),
    sku: 'P070',
    nombre: 'Producto 70',
    categoria: 'Accesorios',
    marca: 'Puma',
    precio: 340022,
    talla: 38,
    color: 'Rojo',
    stock: 50,
    vendidos: 34,
    fechaRegistro: '2025-02-14'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b15b'),
    sku: 'P074',
    nombre: 'Producto 74',
    categoria: 'Calzado',
    marca: 'Puma',
    precio: 295350,
    talla: 'L',
    color: 'Gris',
    stock: 29,
    vendidos: 161,
    fechaRegistro: '2025-12-13'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b15d'),
    sku: 'P076',
    nombre: 'Producto 76',
    categoria: 'Calzado',
    marca: 'Puma',
    precio: 350320,
    talla: 'S',
    color: 'Gris',
    stock: 23,
    vendidos: 38,
    fechaRegistro: '2025-08-25'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b162'),
    sku: 'P081',
    nombre: 'Producto 81',
    categoria: 'Ropa',
    marca: 'Adidas',
    precio: 187085,
    talla: 'S',
    color: 'Azul',
    stock: 2,
    vendidos: 170,
    fechaRegistro: '2025-03-12'
  }
]
Type "it" for more
dafitiDB> db.productos.find({ nombre: /Tenis/i })
[
  {
    _id: ObjectId('691b9de636d8b21a1763b112'),
    sku: 'P001',
    nombre: 'Tenis Running Hombre',
    categoria: 'Calzado',
    marca: 'Adidas',
    precio: 249900,
    talla: 42,
    color: 'Negro',
    stock: 12,
    vendidos: 58,
    fechaRegistro: '2025-01-10'
  },
  {
    _id: ObjectId('691b9de636d8b21a1763b11a'),
    sku: 'P009',
    nombre: 'Tenis Lifestyle Mujer',
    categoria: 'Calzado',
    marca: 'Nike',
    precio: 299900,
    talla: 38,
    color: 'Rosa',
    stock: 15,
    vendidos: 66,
    fechaRegistro: '2025-07-18'
  }
]
dafitiDB> db.productos.aggregate([
...   { $group: { _id: "$categoria", totalProductos: { $sum: 1 } } }
... ])
...
[
  { _id: 'Accesorios', totalProductos: 30 },
  { _id: 'Calzado', totalProductos: 30 },
  { _id: 'Ropa', totalProductos: 40 }
]
dafitiDB> db.productos.aggregate([
...   { $group: { _id: null, totalVendidos: { $sum: "$vendidos" } } }
... ])
...
[ { _id: null, totalVendidos: 9692 } ]
dafitiDB> db.productos.aggregate([
...   { $group: { _id: "$categoria", promedioPrecio: { $avg: "$precio" } } }
... ])
...
[
  { _id: 'Accesorios', promedioPrecio: 217700.16666666666 },
  { _id: 'Calzado', promedioPrecio: 242368.23333333334 },
  { _id: 'Ropa', promedioPrecio: 223349.25 }
]
dafitiDB> db.productos.aggregate([
...   { $group: { _id: "$categoria", totalProductos: { $sum: 1 } } }
... ])
...
[
  { _id: 'Accesorios', totalProductos: 30 },
  { _id: 'Calzado', totalProductos: 30 },
  { _id: 'Ropa', totalProductos: 40 }
]
dafitiDB> db.productos.aggregate([
...   { $group: { _id: "$categoria", precioPromedio: { $avg: "$precio" } } }
... ])
...
[
  { _id: 'Accesorios', precioPromedio: 217700.16666666666 },
  { _id: 'Calzado', precioPromedio: 242368.23333333334 },
  { _id: 'Ropa', precioPromedio: 223349.25 }
]
dafitiDB> db.productos.aggregate([
...   { $group: { _id: "$categoria", promedioPrecio: { $avg: "$precio" } } }
... ])
...
[
  { _id: 'Accesorios', promedioPrecio: 217700.16666666666 },
  { _id: 'Calzado', promedioPrecio: 242368.23333333334 },
  { _id: 'Ropa', promedioPrecio: 223349.25 }
]
dafitiDB> db.productos.aggregate([
...   { $group: { _id: "$marca", totalProductos: { $sum: 1 } } }
... ])
...
[
  { _id: 'North Face', totalProductos: 1 },
  { _id: 'Velez', totalProductos: 15 },
  { _id: 'Totto', totalProductos: 16 },
  { _id: 'Adidas', totalProductos: 10 },
  { _id: 'Nike', totalProductos: 18 },
  { _id: 'Studio F', totalProductos: 19 },
  { _id: 'Puma', totalProductos: 19 },
  { _id: 'Levis', totalProductos: 1 },
  { _id: 'Zara', totalProductos: 1 }
]
dafitiDB> use dafitiDB
already on db dafitiDB
dafitiDB>
