## TP1: Clasificación de los lenguajes
> <a href="https://docs.google.com/spreadsheets/d/1a6mgeLaqPP6j4A0av_z63PFeIYNzUHPpnHn3JcD8C6M/edit" target="_blank" rel="noopener noreferrer">TP1: Clasificación de los lenguajes</a>

## TP2: Análisis de datos
> <a href="https://colab.research.google.com/drive/1BXw_IA4-zQg94kvr6XQLJypS2uxc07YA" target="_blank" rel="noopener noreferrer">TP2: Análisis de datos</a>

## TP3: Problemas de diferentes paradigmas
> <a href="https://docs.google.com/spreadsheets/d/1WhT8OFzteAakbMAd4iq4WLB27z__1Coz/edit?gid=1837626046#gid=1837626046" target="_blank" rel="noopener noreferrer">TP3: Problemas de diferentes paradigmas</a>

## TP4: Identificar la gramática del IF
> <a href="https://drive.google.com/file/d/19GiY930CFI9cpSjTBDYhMptPycup1l8m/view?usp=sharing" target="_blank" rel="noopener noreferrer">TP4: Identificar la gramática del IF</a>

## TP5: Tabla GIC, BNF, EBNF Y ABNF del lenguaje BRA
> GIC  
> Programa         -> começo ListaSentencias final  
> ListaSentencias  -> Sentencia | Sentencia ListaSentencias  
> Sentencia        -> ID ::= Expresion | ler(ListaIDs); | escrever(ListaExpresiones);  
> ListaIDs         -> ID | ID , ListaIDs  
> ListaExpresiones -> Expresion | Expresion , ListaExpresiones  
> Expresion        -> Primaria | Primaria Operador Expresion  
> Primaria         -> ID | Constante | (Expresion)  
> Operador         ->  + | -   

> BNF  
> \<Programa> ::= começo <ListaSentencias> final  
> \<ListaSentencias> ::= \<Sentencia> | \<Sentencia> \<ListaSentencias>  
> \<Sentencia> ::= ID ::= \<Expresion> | ler ( \<ListaIDs> ) ; | escrever ( \<ListaExpresiones> ) ;  
> \<ListaIDs> ::= ID | ID , \<ListaIDs>  
> \<ListaExpresiones> ::= \<Expresion> | \<Expresion> , \<ListaExpresiones>   
> \<Expresion> ::= \<Primaria> | \<Primaria> \<Operador> \<Expresion>  
> \<Primaria> ::= ID | Constante | ( \<Expresion> )  
> \<Operador> ::= + | -  

> EBFN  
> \<Programa> ::= começo \<ListaSentencias> final   
> \<ListaSentencias> ::= { \<Sentencia> }+  
> \<Sentencia> ::= ID ::= \<Expresion> | ler ( \<ListaIDs> ) ; | escrever ( \<ListaExpresiones> ) ;  
> \<ListaIDs> ::= ID { , ID }*  
> \<ListaExpresiones> ::= \<Expresion> { , \<Expresion> }*  
> \<Expresion> ::= \<Primaria> { \<Operador> \<Expresion> }?  
> \<Primaria> ::= ID | Constante | ( \<Expresion> )  
> \<Operador> ::= + | -  

> ABNF  
> _programa_ :  
>         **começo** listaSentencias **final**  
> 
> _listaSentencias_ :  
>         sentencia  
>         sentencia listaSentencias  
> 
> _sentencia_ :  
>         **ID** **::=** expresion  
>         **ler** **(** listaIDs **)** **;**  
>         **escrever** **(** listaExpresiones **)** **;**  
> 
> _listaIDs_ :  
>         **ID**  
>         **ID** **,** listaIDs  
> 
> _listaExpresiones_ :  
>         expresion  
>         expresion **,** listaExpresiones  
> 
> _expresion_ :  
>         primaria  
>         primaria operador expresion  
> 
> _primaria_ :  
>         **ID**  
>         **Constante**  
>         **(** expresion **)**  
> 
> _operador_ :  
>           unode **+** **-**
