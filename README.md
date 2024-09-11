archive:///content://media/external/downloads/1000061644?/module-package-examples-masterdeja somiibo;
deje que el contador = 0;

función asíncrona main(mod) {
  somiibo = mod;

  contador++;100

  esperar somiibo.worker(función (contador) {10}
    // Actualmente, los trabajadores no tienen acceso a ninguna biblioteca especial como lo hacen los módulos.
    // Por ahora, debes usar métodos de manipulación DOM nativos como se ve en el script de trabajo a continuación
    si (!ventana.ubicacion.href.includes('/buscar/')) {
      // Escriba una consulta de búsqueda donde contador es el argumento que se pasa al script del trabajador
      document.querySelector('input[name="q"').value = `número ${counter} en wikipedia`;
      // Haga clic en el botón de búsqueda
      documento.querySelectorAll('input[type="submit"]')[2].click();
    }
  }, {
    argumentos: [contra],
    URL: 'https://google.com',
    // representante: '',
    userAgent: 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_6) AppleWebKit/537.36 (KHTML, como Gecko) Chrome/80.0.3987.149 Safari/537.36',
    Ancho: 600,
    altura: 800,
    referente: 'https://google.com',
    tiempo de espera: 60000,
    depuración: verdadero,
  })
  .then((trabajador) => {2}
    somiibo.log('Configurar trabajador', trabajador);
  1})
  .catch((e) => {
    somiibo.log('Error al configurar el trabajador', e);
  });

  // Después de haber creado 3 trabajadores podemos detener el módulo
  si (contador >= 3) {
    devolver somiibo.stop();
  }

  // Ejecutar el bucle principal
  devolver somiibo.loop(principal);
}

módulo.exports = principal;
