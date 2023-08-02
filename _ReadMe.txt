1. Add prettify
   Add Svelte for VSCode
   Add EsLinte

2. npm create vite@latest svelte-course -- --template svelte

3. npm run dev

Styles will have svelte Class names: class="s-XsEmFtvddWTw"
main.js is our entry point int he App

4. Script will only run once:
    <script>
    
    let count = 0;
    function increment(){
        count += 1;
    }

    let string =`ou have clicked ${count} times`;
    </script>

5. Mapping
    App1 - Counter1/Coutner2/Counter3
    App2 - Counter4