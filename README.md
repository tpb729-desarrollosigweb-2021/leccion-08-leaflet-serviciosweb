# Leaflet - acceso a servicios web
[Leaflet](https://leafletjs.com/) proporciona acceso a servicios WMS mediante la clase TileLayer.WMS.

Para más información, puede revisar el tutorial [Using WMS and TMS services](https://leafletjs.com/examples/wms/wms.html).

## Clases del API de Leaflet

### Clase TileLayer.WMS
La clase [TileLayer.WMS](https://leafletjs.com/reference-1.7.1.html#tilelayer-wms) extiende la clase [TileLayer](https://leafletjs.com/reference-1.7.1.html#tilelayer) para desplegar una capa proveniente de un servicio [WMS](https://es.wikipedia.org/wiki/Web_Map_Service).

Ejemplo de uso:

```javascript
// Agregar capa WMS
var capa_distritos = L.tileLayer.wms('http://geos.snitcr.go.cr/be/IGN_5/wms?', {
  layers: 'limitedistrital_5k',
  format: 'image/png',
  transparent: true
}).addTo(mapa);

control_capas.addOverlay(capa_distritos, 'Distritos');
```

**Ejercicios**  
1. Cree un mapa en Leaflet que incorpore capas de los siguientes servicios WMS:  
  a. [Sistema Nacional de Información Territorial (SNIT)](https://www.snitcr.go.cr/servicios_ogc_completo)  
  b. [Mundialis](https://www.mundialis.de/en/ows-mundialis/)
