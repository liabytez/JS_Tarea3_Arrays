# JS_Tarea3_Arrays

## Autora
Hailie Mountain

## Enunciados

### Ejercicio 1: Números pares
Dado el array numeros, usa filter para obtener solo los números pares. Un número es par si n % 2 === 0.
 

const numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const pares = numeros.filter(/* completa aquí */);
console.log(pares);

### Ejercicio 2: Filtrar por propiedad de objeto
Filtra el array productos para obtener solo los que tienen stock > 0.

const productos = [
  { nombre: "Manzana",  precio: 1.2,  stock: 50 },
  { nombre: "Kiwi",     precio: 0.8,  stock: 0  },
  { nombre: "Mango",    precio: 2.5,  stock: 12 },
  { nombre: "Papaya",   precio: 3.0,  stock: 0  },
  { nombre: "Naranja",  precio: 0.6,  stock: 30 },
];
const disponibles = productos.filter(/* completa aquí */);

### Ejercicio 3: Eliminar duplicados

Elimina los valores duplicados del array tags usando filter e indexOf. Pista: un elemento es único si su posición actual coincide con la primera vez que aparece.

const tags = ["js", "css", "js", "html", "css", "js", "react"];
const unicos = tags.filter(/* completa aquí */);
console.log(unicos);

### Ejercicio 4: Precios con IVA

Dado el array precios, usa map para calcular el precio final con 21% de IVA. Redondea a 2 decimales con toFixed(2) y convierte a número con Number().

const precios = [10, 25.5, 8.99, 100, 49.95];
const conIVA = precios.map(/* completa aquí */);
console.log(conIVA);

### Ejercicio 5: Extraer propiedades con destructuring
Usa map con destructuring en el parámetro para extraer solo nombre y edad de cada usuario, creando objetos nuevos más simples.

const usuarios = [
  { id: 1, nombre: "Ana",   edad: 23, ciudad: "Madrid"    },
  { id: 2, nombre: "Luis",  edad: 31, ciudad: "Barcelona" },
  { id: 3, nombre: "Marta", edad: 19, ciudad: "Sevilla"   },
];
const resumen = usuarios.map(/* usa destructuring aquí */);
console.log(resumen);

### Ejercicio 6: Formatear strings
Convierte el array de nombres a formato "APELLIDO, Nombre" usando map y el método split(" ") para separar nombre y apellido.
 

const nombres = [
  "ana garcia",
  "luis perez",
  "marta lopez",
  "carlos ruiz"
];
// Resultado esperado: ["GARCIA, Ana", "PEREZ, Luis", ...]
const formateados = nombres.map(/* completa aquí */);
console.log(formateados);

### Ejercicio 7: Suma total
Calcula la suma total de los precios usando reduce. El acumulador empieza en 0.
 

const precios = [12.5, 8.99, 45.0, 3.25, 22.8];
const total = precios.reduce(/* completa aquí */, 0);
console.log("Total:", total.toFixed(2));

### Ejercicio 8: Agrupar por categoría
Agrupa el array gastos en un objeto donde cada clave es una categoría y su valor es la suma de esa categoría. El valor inicial es un objeto vacío {}.
 

const gastos = [
  { concepto: "Pizza",      categoria: "comida",   importe: 12 },
  { concepto: "Bus",        categoria: "transporte", importe: 2.5 },
  { concepto: "Sushi",      categoria: "comida",   importe: 18 },
  { concepto: "Cine",       categoria: "ocio",     importe: 9  },
  { concepto: "Taxi",       categoria: "transporte", importe: 8  },
  { concepto: "Concierto",  categoria: "ocio",     importe: 35 },
];
const porCategoria = gastos.reduce(/* completa aquí */, {});
console.log(porCategoria);

### Ejercicio 9: Contar ocurrencias
Cuenta cuántas veces aparece cada palabra en el array palabras. Resultado: un objeto { palabra: cantidad }.
 

const palabras = [
  "hola", "mundo", "hola", "js", "mundo",
  "hola", "filter", "js", "hola"
];
const conteo = palabras.reduce(/* completa aquí */, {});
console.log(conteo);

### Ejercicio 10: Buscar usuario por id

Usa find para buscar el usuario con id === 3. Si no existe, find devuelve undefined.

const usuarios = [
  { id: 1, nombre: "Ana",   rol: "admin" },
  { id: 2, nombre: "Luis",  rol: "user"  },
  { id: 3, nombre: "Marta", rol: "user"  },
  { id: 4, nombre: "Carlos",rol: "admin" },
];
const encontrado = usuarios.find(/* completa aquí */);
console.log(encontrado);

### Ejercicio 11: findIndex y actualizar elemento
Usa findIndex para localizar la posición del producto "Kiwi" en el array. Luego actualiza su precio a 1.5 usando el índice encontrado.
 

const productos = [
  { nombre: "Manzana", precio: 1.2 },
  { nombre: "Kiwi",    precio: 0.8 },
  { nombre: "Mango",   precio: 2.5 },
];
const idx = productos.findIndex(/* completa aquí */);
if (idx !== -1) {
  // actualiza el precio del producto encontrado
}
console.log(productos);

### Ejercicio 12: Ordenar números y strings
Ordena edades de menor a mayor, y frutas alfabéticamente. Recuerda: sin función comparadora, sort ordena como strings (¡bug clásico!).
 

const edades = [31, 5, 18, 42, 7, 23];
const frutas = ["mango", "apple", "kiwi", "banana"];
const edadesOrden = [...edades].sort(/* numérico ascendente */);
const frutasOrden = [...frutas].sort(/* alfabético */);
console.log(edadesOrden);
console.log(frutasOrden);

### Ejercicio 13: Ordenar objetos por propiedad

Ordena el array empleados por salario de mayor a menor. Para invertir el orden, resta al revés: b - a.
 

const empleados = [
  { nombre: "Ana",    salario: 2800 },
  { nombre: "Luis",   salario: 3500 },
  { nombre: "Marta",  salario: 2200 },
  { nombre: "Carlos", salario: 4100 },
];
const ordenados = [...empleados].sort(/* salario descendente */);
ordenados.forEach(e => console.log(e.nombre, "→", e.salario));

### Ejercicio 14: Efectos secundarios y acumulación
Usa forEach para: (1) mostrar cada producto con su precio formateado, y (2) calcular el total acumulando en una variable externa.
 

const carrito = [
  { nombre: "Teclado",  precio: 45.99 },
  { nombre: "Ratón",    precio: 19.5  },
  { nombre: "Monitor",  precio: 199.0 },
  { nombre: "Webcam",   precio: 34.99 },
];
let total = 0;
carrito.forEach(/* muestra cada línea y acumula total */);
console.log("─────────────────");
console.log("Total:", total.toFixed(2) + " €");

### Ejercicio 15: Verificar permisos
Cada usuario tiene un array de roles. Usa includes para verificar si puede acceder a una ruta protegida que requiere el rol "admin". Muestra un mensaje distinto según el resultado.
 

const usuarios = [
  { nombre: "Ana",    roles: ["admin", "editor"] },
  { nombre: "Luis",   roles: ["user"]             },
  { nombre: "Marta",  roles: ["editor", "user"]   },
  { nombre: "Carlos", roles: ["admin"]             },
];
usuarios.forEach(usuario => {
  const puedeAcceder = /* usa includes para comprobar rol "admin" */;
  const mensaje = puedeAcceder
    ? usuario.nombre + ": Acceso permitido"
    : usuario.nombre + ": Acceso denegado";
  console.log(mensaje);
});

### Ejercicio 16: Pipeline completo
A partir de pedidos: (1) filtra los entregados, (2) calcula el total con IVA de cada uno con map, (3) ordénalos de mayor a menor importe, (4) muestra el resultado con forEach.
 

const pedidos = [
  { id: "P01", importe: 45.0,  entregado: true  },
  { id: "P02", importe: 120.0, entregado: false  },
  { id: "P03", importe: 33.5,  entregado: true  },
  { id: "P04", importe: 89.0,  entregado: true  },
  { id: "P05", importe: 15.0,  entregado: false  },
];
pedidos
  .filter(/* solo entregados */)
  .map(/* añadir importeConIVA = importe * 1.21 */)
  .sort(/* de mayor a menor por importeConIVA */)
  .forEach(/* muestra: "P01 → 54.45 €" */);
