# The-use-of-comments-in-code  
By Mr. Manuel Rosendo Castro Iglesias. 2022  
The use of comments in code. Part 1.  
 A comment is a part of code that is not interpreted by the browser and whose usefulness lies in facilitating reading to the programmer.  

 The programmer, as he develops the script, leaves phrases or single words, called comments, that help him or anyone else to read the script more easily when modifying or debugging it.  

 There are many different types of comments in programming languages.  
 Line comments. // The double forward slash (the divide), and serves to comment a line of code to where it ends.  
  ```//Este es un comentario de una línea```
 Block comments. /* ... */
VERY IMPORTANT! NEVER, EVER USE THEM INSIDE A LINE OF CODE. Instead of helping, they just pollute it.
The asterisk bar, we can use it to comment several lines and is indicated with the signs: /* to start the comment and with */ to finish it.
/*
  Este comentario se puede extender
  por varias líneas.
  Sí, las que necesites.
*/
 Documentation comments. /** ... */ It is a very important type of comment that some props use to generate self-documentation. And I especially like to highlight JSDOC. TypeScript also uses them to embed static types.
/**
  ...
  ver instrucciones de uso en el enlace anterior.
  ...
*/
 Region comments. //#region ... //#endregion
It is a very useful type of comment, since it allows you to define collapsible blocks of code, and thereby organize the code into Sections, SubSections, Sub-Sections... Subsections, etc.
Achieving with this sectioning it before dividing it into modules or separate files, avoiding unnecessary refactoring by being able to analyze and organize the code in advance.
By contracting the code within regions, the existing structuring can be better appreciated and understood.
//#region MiRegion:  
... instrucciones  
//#region MiSubregion:  
  ... instrucciones  
//endregion MiSubregion:  
... instrucciones  
//endregion MiRegion:  
//#region MiOtraRegion:  
...  
//#region MiSubregion:  
  ... instrucciones  
  //#region MiSubSubregion:  
    ... instrucciones  
  //endregion MiSubSubregion:  
  ... instrucciones  
//endregion MiSubregion:  
... instrucciones  
//endregion MiOtraRegion:  
Comentarios TODO. //TODO Pendientes Este tipo de comentario se utiliza para indicar cosas pendientes o ideas que solemos tener para mejorar el código, pero no pensamos o podemos realizar en ese momento.

Ejemplos:
//TODO Algo incompleto o pendiente.
  //TODO algo que hacer(001):
//TODO Necesario refactorizar.
//TODO ¿Se podría mejorar usando aquí function* (funciones generadoras)?.
¡Y para mí los más importantes...!
#### Los comentarios de codificación o de colaboración.
 switchComments or toggleComments. Viene en dos sabores:
Los dos son lo mismo y funcionan igual, y por eso uso para ellos dos nombres distintos, y así poder diferenciarlos según su caso de uso.
 switchComments.
/*/ ...comentado... //*/
//*/ ...descomentado... //*/
Este tipo de comentario se debe utilizar:
Cuando necesitamos implemetar algo en el código, pero no queremos que se ejecute, es decir, necesitamos comentarlo o descomentarlo de una manera rápida para activar cosas sin contaminar el resto del código.
Cuando preparamos una demostración, un taller o un curso. Permitiendo activar y desactivar ejemplos o secciones del código, evitando que estorben.
Obsevaciones: Es importante recordar en esta variante, iniciar y cerrar el switchComment antes de abrir uno diferente; ya que de no hacerlo caerás en el toggleComment.
Sugerecias:
Combinar con ```//#region ... //#endregion```  
Combinar con //TODO algo:  
O mejor aún, con una combinación de ambas.  
 toggleComments.  
/*/ ...comentado... /*/ ...descomentado... //*/  
//*/ ...descomentado... /*/ ...comentado... //*/  
Este tipo de comentario se debe utilizar:  
Cuando necesitamos refactorizar. Nos permite tener dos o más variaciones del código y verificar que cumplen con las necesidades y su posible mejora.
Cuando varias personas colaboran en el desarrollo. Permitiendo proponer cambios sin alterar la funcionalidad del código.
"No existe cosa más molesta que venga alguien a decirte ¿y si ... ? y te modifica el código sin siquiera preguntar el porqué lo habías hecho de esa forma." Puede ser una idea GENIAL, pero cuando te tocan, o tocas tú, el código creas un ambiente cargado, que propicia el rechazo casi de forma automática e irracional, por muy buena que sea la idea.
Ejemplos:
  /*/ // switchComment
    ...comentado... 
  /*/ 
    ...descomentado...
  //*/

  /*/  //toggleComment
    ...comentado... 
  /*/
    ...descomentado...
  /*/ 
    ...comentado... 
  /*/ 
    ...descomentado...
  /*/ 
    ...comentado... 
  /*/ 
    ...descomentado...
  //*/
 ALL Make an example with the use of all of them.
