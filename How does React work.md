#work #webdev #frontend
Core react does work around three basic components
1. **React core** -> defining the components
	1. Sdileny s React Nativem
2. **React renderer** -> creating the component tree
	1. For the web, or for the mobile React native does the job
3. **React reconsiler** -> deciding which part of tree to rerender
	1. React compering DOM with React element tree VDOM with each render cycle -> **only necessary changes to DOM** 

Also uses syntax sugar of JSX that is converted with [[Transpilers]], most often Babel, to JS.

Each component goes through [[React component lifecycle]].
To manage state and side effect we use [[React hooks]].


## Client server interaction
Standartne React pouziva [[Client side rendering]] 
1. Server posle HTML file s root <div/> elementem na kterem se stavi React aplikace
2. Server posle JS file, ktery je bundlet v optimalizovanym formatu pomoci nejakeho [[Bundler]] napr. webpack
	1. This is the react app
	2. Nemusi vzdy prijit cela najednou - vyuziva se [[Lazy loading]] viz. [[React lazyloading]]
3. Server posle staticky shit jako obrazky a CSS

Cool people vyuzivaji [[Server side rendering]]
1. Server vyrendruje React aplikaci u sebe, pred tim muze udelat nejaky serverside data fetching
2. Z react aplikace vytvori HTML, které pošle clientovi
3. Proběhne [[Hydration]] a stranka je interaktivni












