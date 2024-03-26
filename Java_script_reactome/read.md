How can we use and improve this Reactome widget so we can view the "Circadian Rhythm" pathway?

![More information can be found on the Reactome tutorial]([https://plantreactome.gramene.org/index.php?option=com_content&view=article&id=58&Itemid=306&lang=en)

____

```html
<script type="text/javascript" language="javascript" src="http://plantreactome.gramene.org/DiagramJs/diagram/diagram.nocache.js"></script>


<div id="diagramHolder"></div>

    function onReactomeDiagramReady(){  
        var diagram = Reactome.Diagram.create({
            "placeHolder" : "diagramHolder",
            "width" : 900,
            "height" : 500
        });

        
        diagram.loadDiagram("R-OSA-8933811");

        //Adding different listeners

        diagram.onDiagramLoaded(function (loaded) {
            console.info("Loaded ", loaded);
            diagram.selectItem("R-OSA-8933811");
            diagram.flagItems("ELF3");
        });

        diagram.onObjectHovered(function (hovered){
            console.info("Hovered ", hovered);
        });

        diagram.onObjectSelected(function (selected){
            console.info("Selected ", selected);
        });
    }
```

---
