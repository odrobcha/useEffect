##Creat React Project with Vite
Documentation  https://vitejs.dev/guide/why.html
- install node.js
- `npm create vite@latest`
    - type the name
    - chose the framework
    - chose the lang
- cd "to the folder where the project is located"
- `npm install`
- `npm run dev`


## SideEffect
Is the tasks that need to be executed that do NOT impact the current component render cycle

useEffect(()=>{
  sideEffectFunction
}, [])

useEffect function will execute if the dependency array is changed

### Dependency array
    - [] - sideEffectFunction executes once, after component function is executed
    - null - sideEffectFunction executes every time components function rerenders
