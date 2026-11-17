# Control de Bóveda

Aplicación web (un solo archivo HTML) para llevar el control de la bóveda de un casino.

## Uso

Abre `index.html` con doble clic en Chrome o Edge. Los datos se guardan en el navegador (localStorage); usa **Inicio → Descargar respaldo** para guardar una copia `.json`.

Los gráficos (Chart.js) y el PDF (jsPDF) se cargan desde internet.

## Secciones

1. **Inicio**: monto total (efectivo + Izipay), efectivo en bóveda, Izipay, gastos, retiros, reposiciones internas y externas, pérdidas y ganancia neta.
2. **Registrar**: bóveda inicial y registros por periodo (recuento de caja cada 1, 2, 3 o más días) con ganancia, Izipay, pérdida de caja, reposiciones, gastos y retiros con detalle.
3. **Gráficos**: barras mensuales por año.
4. **Reportes PDF**: filtro por fechas y tipo, descarga en PDF.

## Cálculos

- **Efectivo en bóveda** = bóveda inicial + ganancia en efectivo − reposición a caja − gastos − retiros
- **Pérdida**: es de la caja; no resta directo a la bóveda. Se cubre con reposición a caja (desde bóveda, hasta lo disponible) y, si no alcanza, con reposición externa.
- **Izipay**: ganancia que no entra a la bóveda.
- **Ganancia neta** = ganancia en efectivo + Izipay − pérdidas − gastos

Ejemplo: pérdida de caja de S/ 1,520 con S/ 20 en bóveda → reposición a caja S/ 20 + reposición externa S/ 1,500.
