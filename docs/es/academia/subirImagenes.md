# Informe completo sobre ImgBB e imgbox
*(para subir imágenes y poder incrustarlas en cualquier web sin usar su propio servidor)*

---

## Introducción
Este informe está específicamente orientado a la necesidad de **subir imágenes a un servicio externo y poder incrustarlas (hotlink) en cualquier web**, sin usar el almacenamiento propio de esa web.  
Se analizan dos servicios: **ImgBB** y **imgbox**, incluyendo planes gratuitos y de pago, formatos soportados, límites, API, proceso de subida y términos de uso.

---

# ImgBB (ibb.co / imgbb.com)

## Qué es y para qué sirve
ImgBB es un host de imágenes orientado a compartir con **enlaces directos** y códigos de inserción (HTML/BBCode).  
Permite:
- Arrastrar y soltar imágenes.
- Pegar desde el portapapeles.
- Subir por URL.

Opcionalmente ofrece **borrado automático** y muestra **códigos de inserción listos**.

## Formatos, tamaño y funciones clave
- **Formatos**: JPG, PNG, BMP, GIF, TIF, WEBP, **HEIC**, **AVIF**, incluso **PDF**.
- **Límite por archivo (gratis)**: **32 MB**.
- **Códigos de inserción**: enlace del visor, **HTML enlazado**, miniaturas HTML, **BBCode**.
- **Privacidad de álbumes**: Público, privado con enlace o **privado con contraseña**.
- **Autoborrado**: desde 5 minutos hasta 6 meses al subir.

## Planes y precios
- **Pro Mensual**: 12,99 $/mes
- **Pro Anual**: 7,99 $/mes (95,88 $)
- **Pro 3 años**: 3,99 $/mes (143,64 $)

**Ventajas Pro**:
- Sin anuncios.
- **Direct Linking** (garantizado).
- Espacio ilimitado.
- **Reemplazar imagen**.
- **64 MB** por imagen.
- **API Access**.

> Nota: aunque en la práctica el plan gratuito ya ofrece enlaces directos, el plan Pro los garantiza formalmente y añade funciones avanzadas.

## Cómo subir y obtener un enlace para incrustar
1. Ir a **Upload** y arrastrar la imagen (o pegar/URL).
2. (Opcional) Configurar **Auto delete** y/o redimensionar.
3. Tras subir, copiar uno de los **Embed codes**:
    - **HTML full linked** → para `<img src="…">`.
    - **BBCode** → foros.
    - O la **Direct image link**.

Ejemplo en HTML:
```html
<img src="https://i.ibb.co/XXXX/miimagen.jpg" alt="Descripción">
```

# imgbox (imgbox.com)

## Qué es y para qué sirve
imgbox es un servicio **gratuito** y muy simple para alojar y **enlazar directamente** imágenes.  
La home expone sus límites básicos y que funciona bajo **SSL**.

---

## Formatos, tamaño y funciones clave
- **Formatos**: JPG, GIF y PNG.  
- **Límite por archivo**: 10 MB.  
- **Almacenamiento**: “lifetime” (sin caducidad) mientras no se violen los TOS.  
- **Hotlink/ancho de banda**: sin límite duro; pueden bloquear referers abusivos.  

---

## Planes y precios
- Solo existe el plan **gratuito**.  
- No hay planes de pago anunciados.  

---

## Cómo subir y obtener un enlace para incrustar
1. Ir a **UPLOAD IMAGES** y arrastrar/seleccionar archivos.  
2. Tras subir, abrir la imagen en tamaño completo.  
3. Copiar la **URL directa** (termina en `.jpg`, `.png` o `.gif`) y usarla en HTML/Markdown:

```html
<img src="https://images#.imgbox.com/ruta/archivo.jpg" alt="Descripción">
```

## Términos y restricciones
- Hotlink permitido sin límite de tráfico “duro”.
- El servicio puede bloquear consumos abusivos.
- Servicio provisto “tal cual” y con derecho a retirar contenido ilegal/abusivo.

---

## Comparativa rápida

| Aspecto             | ImgBB                                          | imgbox                           |
|----------------------|-----------------------------------------------|----------------------------------|
| **Gratis / Pago**    | Gratis; Pro desde 3,99–12,99 $/mes            | Solo gratis                      |
| **Límite por imagen**| 32 MB (gratis) / 64 MB (Pro)                  | 10 MB                            |
| **Formatos**         | JPG/PNG/GIF/BMP/TIF/WEBP/HEIC/AVIF/PDF        | JPG/PNG/GIF                      |
| **Hotlink**          | Enlaces directos y códigos; sin cuota pública (pueden mitigar abusos) | Sin límite duro; bloquean referers abusivos |
| **Privacidad/álbum** | Público, privado, contraseña                  | Sin perfiles; acceso solo por URL |
| **Extras**           | Autoborrado, API, plugin, reemplazar (Pro)    | Simplicidad + SSL                 |
| **Uso recomendado**  | Imágenes grandes, formatos modernos, API o caducidad | Sencillez y hotlink rápido (≤10 MB) |

---

## Recomendaciones prácticas
- **Para posts con imágenes ≤10 MB y máxima sencillez**: usar **imgbox**.  
  Su política de “sin límite duro” de ancho de banda lo hace ideal para hotlink estable (siempre que no haya abusos).

- **Para imágenes más pesadas, formatos modernos (WEBP/AVIF/HEIC) o caducidad automática**: usar **ImgBB**.
