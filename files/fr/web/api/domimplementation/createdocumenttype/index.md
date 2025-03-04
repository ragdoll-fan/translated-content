---
title: DOMImplementation.createDocumentType()
slug: Web/API/DOMImplementation/createDocumentType
tags:
  - API
  - DOM
  - DOMImplementation
  - Méthode
  - Reference
translation_of: Web/API/DOMImplementation/createDocumentType
---
{{ ApiRef("DOM")}}

La méthode **`DOMImplementation.createDocumentType()`** renvoie un objet {{domxref("DocumentType")}}  qui peut être utilisé avec {{domxref("DOMImplementation.createDocument")}} lors de la création du document ou peut être intégré au document existant avec des méthodes comme {{domxref("Node.insertBefore()")}} ou {{domxref("Node.replaceChild()")}}.

## Syntaxe

    doctype = document.implementation.createDocumentType(qualifiedNameStr, publicId, systemId)

### Paramètres

- _qualifiedNameStr_
  - : est une {{domxref("DOMString")}} (_chaîne de caractères_) contenant le nom qualifié comme `svg:svg`.

<!---->

- _publicId_
  - : est une {{domxref("DOMString")}} (_chaîne de caractères_) contenant l'identifiant `PUBLIC`.

<!---->

- _systemId_
  - : est une {{domxref("DOMString")}} (_chaîne de caractères_) contenant les identifiants `SYSTEM`.

## Exemple

```js
var dt = document.implementation.createDocumentType('svg:svg', '-//W3C//DTD SVG 1.1//EN', 'http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd');
var d = document.implementation.createDocument('http://www.w3.org/2000/svg', 'svg:svg', dt);
alert(d.doctype.publicId); // -//W3C//DTD SVG 1.1//EN
```

##  Spécifications

| Spécification                                                                                                                                        | Statut                           | Commentaire                                             |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- | ------------------------------------------------------- |
| {{SpecName('DOM WHATWG', '#dom-domimplementation-createdocumenttype', 'DOMImplementation.createDocumentType')}} | {{Spec2('DOM WHATWG')}} | Pas de modification de {{SpecName("DOM3 Core")}} |
| {{SpecName('DOM3 Core', 'core.html#Level-2-Core-DOM-createDocType', 'DOMImplementation.createDocumentType')}}     | {{Spec2('DOM3 Core')}}     | Pas de modification de {{SpecName("DOM2 Core")}} |
| {{SpecName('DOM2 Core', 'core.html##Level-2-Core-DOM-createDocType', 'DOMImplementation.createDocumentType')}} | {{Spec2('DOM2 Core')}}     | Définition initiale.                                    |

## Compatibilité des navigateurs

{{Compat("api.DOMImplementation.createDocumentType")}}

## Voir aussi

- L'interface {{domxref("DOMImplementation")}} à laquelle elle appartient.
