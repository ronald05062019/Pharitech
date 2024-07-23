# Diagrama BPMN

<p id="bpmn-viewer"></p>

<script src="https://unpkg.com/bpmn-js@8.5.0/dist/bpmn-viewer.development.js"></script>
<script>
  // URL del archivo BPMN subido
  var url = 'WatchTower.bpmn';

  var BpmnViewer = window.BpmnJS;
  var viewer = new BpmnViewer({ container: '#bpmn-viewer' });

  fetch(url).then(response => response.text()).then(xml => {
    viewer.importXML(xml, function(err) {
      if (err) {
        console.error('error rendering', err);
      } else {
        console.log('rendered');
      }
    });
  });
</script>
