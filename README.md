**<br>Nama : Fathin Muhashibi Putra**
**<br>NRP : 5025211229**
**<br>Kelas : Grafika Komputer A**
**<br>Tahun : 2023**

# ASSIGNMENT 3 (RGB Triangle and 3D Cube in WebGL)

**Dokumentasi :**

## 1. RGB Triangle in WebGL

### Triangle 1 :
```
 /* SEGITIGA KE-1 */

    /* Koordinat segitiga ke-1 : */
    /* Set up values for the "coords" attribute */

    let  coords1 = new Float32Array( [ -0.5,-0.5, 0.5,0.5, -0.5,0.5 ] );
            
    gl.bindBuffer(gl.ARRAY_BUFFER, bufferCoords);
    gl.bufferData(gl.ARRAY_BUFFER, coords1, gl.STREAM_DRAW);
    gl.vertexAttribPointer(attributeCoords, 2, gl.FLOAT, false, 0, 0);
    gl.enableVertexAttribArray(attributeCoords); 
   
    /* Warna segitiga ke-1 : */
    /* Set up values for the "color" attribute */
   
    let  color = new Float32Array( [ 0,1,0, 1,0,0, 0,0,1 ] );

    gl.bindBuffer(gl.ARRAY_BUFFER, bufferColor);
    gl.bufferData(gl.ARRAY_BUFFER, color, gl.STREAM_DRAW);
    gl.vertexAttribPointer(attributeColor, 3, gl.FLOAT, false, 0, 0);
    gl.enableVertexAttribArray(attributeColor); 
    
    /* Gambar segitiga ke-1 :*/
    /* Draw the triangle. */
   
    gl.drawArrays(gl.TRIANGLES, 0, 3);
```
<img width="374" alt="image" src="https://github.com/fathinmputra/assignment3_webgl/assets/103252800/68779462-f9d3-4757-9314-aba03d75cfa7">


### Triangle 2 :
```
/* SEGITIGA KE-2 */

    /* Koordinat Segitiga ke-2 : */
    /* Set up values for the "coords" attribute */

    let  coords2 = new Float32Array( [ -0.5,-0.5, 0.5,0.5, 0.5,-0.5 ] );
            
    gl.bindBuffer(gl.ARRAY_BUFFER, bufferCoords);
    gl.bufferData(gl.ARRAY_BUFFER, coords2, gl.STREAM_DRAW);
    gl.vertexAttribPointer(attributeCoords, 2, gl.FLOAT, false, 0, 0);
    gl.enableVertexAttribArray(attributeCoords); 
   
    /* Warna segitiga ke-2 : */
    /* Set up values for the "color" attribute */
   
    let  color2 = new Float32Array( [ 0,1,0, 1,0,0, 1,1,1 ] );

    gl.bindBuffer(gl.ARRAY_BUFFER, bufferColor);
    gl.bufferData(gl.ARRAY_BUFFER, color2, gl.STREAM_DRAW);
    gl.vertexAttribPointer(attributeColor, 3, gl.FLOAT, false, 0, 0);
    gl.enableVertexAttribArray(attributeColor); 
    
    /* Gambar segitiga ke-2 :*/
    /* Draw the triangle. */
   
    gl.drawArrays(gl.TRIANGLES, 0, 3);
```
<img width="375" alt="image" src="https://github.com/fathinmputra/assignment3_webgl/assets/103252800/a7d6ad1b-c344-4ac5-ab2c-fee9d5708769">


### Result :
<img width="373" alt="image" src="https://github.com/fathinmputra/assignment3_webgl/assets/103252800/5c14dc8f-30c9-405b-befe-a519647da71e">


## 2. 3D Cube WebGL

```
    drawPrimitive( gl.TRIANGLE_FAN, [0,1,0,1], [ -0.6,-0.5,-0.5, -0.6,0.3,-0.5, 0.2,0.3,-0.5, 0.2,-0.5,-0.5 ]); //depan (hijau)
    drawPrimitive( gl.TRIANGLE_FAN, [1,0,0,1], [ 0.4,-0.3,0.5, -0.4,-0.3,0.5, -0.4,0.5,0.5, 0.4,0.5,0.5 ]); //belakang (merah)
    drawPrimitive( gl.TRIANGLE_FAN, [0,0,1,1], [ -0.6,-0.5,0.5, -0.4,-0.3,0.5, -0.4,0.5,0.5, -0.6,0.3,0.5 ]); //samping kiri (biru)
    drawPrimitive( gl.TRIANGLE_FAN, [1,1,0,1], [ 0.2,-0.5,-0.5, 0.2,0.3,-0.5, 0.4,0.5,-0.5, 0.4,-0.3,-0.5 ]); //samping kanan (kuning)
    drawPrimitive( gl.TRIANGLE_FAN, [1,0,1,1], [ -0.6,0.3,0.5, -0.4,0.5,0.5, 0.4,0.5,-0.5, 0.2,0.3,-0.5 ]); //atas (ungu)
    drawPrimitive( gl.TRIANGLE_FAN, [0,1,1,1], [ -0.6,-0.5,0.5, -0.4,-0.3,-0.5, 0.4,-0.3,-0.3, 0.2,-0.5,-0.5 ]); //bawah (cyan/biru muda)

```

### Sisi Depan dan Belakang
<img width="372" alt="image" src="https://github.com/fathinmputra/assignment3_webgl/assets/103252800/28273a62-4078-49d3-b0b2-9f1d971e239b">

### Sisi Kiri dan Kanan
<img width="373" alt="image" src="https://github.com/fathinmputra/assignment3_webgl/assets/103252800/984b290b-8b4a-466f-a549-0b4415a71d72">

### Sisi Atas dan Bawah
<img width="373" alt="image" src="https://github.com/fathinmputra/assignment3_webgl/assets/103252800/0501d13a-4300-434f-8b01-2b34a37848da">





