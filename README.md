# Jonathan's Roadmap Wishlist

## Front-End Framework's / Libraries
- [Vue.js](https://vuejs.org/)
	- Keep codebase consistent with Discovery app
	- Highly opinionated framework will keep things consistent
- [Vuex](https://vuex.vuejs.org/guide/)
	- Global store will faciliate moving information between components
	- Adds cacheing capabilities to limit requests across the wire
	- Centralizes shared data and makes it easier to reason about
- Single Page Application via [Vue Router](https://router.vuejs.org/guide/)
	- Better user experience (no hard reloads)
	- Can add transitions between different sections
	- Allows us to modularize and re-use UI components (i.e. modals or user-card)
- [ESLint](https://eslint.org/)
	- Actually enforce all the requirements (Satya built in workarounds in the config file)
	- Would like to customize our rules some more (i.e. enfore snake case as per Rohan's preference, and enforce 4 space tabs as per my preferences)
	- Currently we are using a hacked up version of the [AirBnB styleguide](https://github.com/airbnb/javascript)
- [Webpack](https://webpack.js.org/) & [Babel](https://babeljs.io/)
	- Webpack allows us to bundle and minify our JS so that we can build out a dependancy chain
	- Much easier to reason about our code
	- Babel will transpile and poyfill so our code works with all browsers
	- Babel and Webpack together allow us to leverage all ES6+ features i.e. imports and async await
- [Jest](https://jestjs.io/)
	- Unit testing, snapshot UI testing
	- Chose this because it is suggested by Vue core team
	- Integrates well with Vue ecosystem and has many libraries/large community
- [Typescript](https://www.typescriptlang.org/)
	- Type safety for compile time errors rather than runtime errors
	- This will be increasingly important as we become more hands off with advisors
	- AKA making sure they cant fuck things up from the UI
	- Better intellisense for manouvering around code
	- Vue is offering more and more support for typescript (Entire vue codebase is now written in typescript)
- Testing
	- Ideally have 100% test coverage of the front-end and back-end

#### Conclusion
Implementing all of this will require a complete re-write of the front-end. I anticipate it would take about a month of dedicated work to completely transition to these libraries and frameworks. As for overhead, with all the ad-hoc dependencies in the current project, and with good bundling/minifying in the future state, I think the total weight of our front end will decrease. I have a vue project that uses all the above dependencies, and I could do some benchmarking if performance is a concern.

We could also go with React, there are generally more React developers and React offers more freedom and therefore more scalability. However, it is less opinionated and therefore there is more room for development styles to diverge and lead to a messy codebase. There are tradeoffs to both.

>NOTE: All of the technologies I have suggested are industry standard or at least considered best practices

## Node.js Codebase
- Re-factor pdf_generator.js so that each section is a function call that gets passed requisite data
	- This will allow us to generate different account opening apps easily (i.e. joint vs non-joint)
- server.js would have to be heavily re-factored if moving to an SPA

#### Conclusion
Backend is pretty clean in my estimation.