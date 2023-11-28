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
!!!! useEffectex ecutes when component is rendered

useEffect(()=>{
  sideEffectFunction
}, [])

useEffect function will execute if the dependency array is changed

### Dependency array
    - [] - sideEffectFunction executes once, after component function is executed
    - null - sideEffectFunction executes every time components function rerenders
    - [VAR] - sideEffectFunction executes every time VAR changes
    - useEffect(()=>{
         sideEffectFunction;
         return ()=>{
            cleanFunction  - clean the sideEffectFunction right before sideEffectFunction runs again or before is dismounts
    }
    }, [])

    - if function as dependency - can create infinite loop, if inside the sideEfeectFunction the state is changed
        to prevent it use - useCallback. To prevet recreate new fnction everytime.
        Call useEffect(Func(that should not be recreated everyTime), [Dependencies]); Dependencyies - whent it changes Func is recreated
