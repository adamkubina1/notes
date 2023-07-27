## useState
Pro ukládání stavu, který přímo souvisí s vizuálním vzhledem komponentu

#pitfall po zavolani setter funkce se state updatne az pri dalsim render - tedy pokud po zavolani setteru dame console.log() statu, tak tam bude ten stary

## useEffect
Pro práci s vedlejšími efekty komponentu během [[React component lifecycle]]

## useRef
Pro ukládání stavu, který nesouvisí se vzhledem komponentu -> je oddělený od [[React component lifecycle]].
Hodnota se neresetuje mezi rerenders a její změna netrigruje rerender.

#pitfall ref.current vubec nepatri do vizualu tedy nedavat do JSX

## useMemo
Pro optimalizaci useEffectu pokud tam jsou narocne kalkulace -> nebo? to nechceme dělat při každým rerender.

Probehne jednou a pak je vysledek cached ([[Memoization]]), probiha znovu jen pri zmenach v dependency array.

## useCallback
Pro optimalizaci useEffectu - na rozdil od useMemo vraci celou funkci ne hodnotu.

Pokud mezi rerender nechceme aby se funkce zmenila pouzijem napr. pokud memo() komponentu passujeme funkci

## useContext
Pro passovani hodně hlubokých props mezi komponenty

Vypada to jako vice kontrolovana alternativa global variables.
Jedna z možností globálního [[State managment]] v Reactu - context, providers


## useReducer
Pro zjednodušení složitého state managmentu komponentu - alternativa useState.

#pitfall Komponent state ne globální state.


## V kostce
#### State jednoho komponentu
- useState
- useRef
- useReducer
#### State více komponentu
- useContext
#### Vedlejší efekty
- useEffect
- useMemo
- useCallback
