<H1 align="center">Next Search</H1>
<p align="center">🚀Creation of a search structure in Next for future references</p>


## Requirements
- Next
- heroicons
- clsx
- use-debounce


 <div align="center">
 <h2>Default</h2>
 <img src="https://github.com/lucasmargui/React_Estrutura_Search-Table/assets/157809964/cb78f54d-cb72-4d99-a01c-49b94403ef36" style="width:100%">
 <h2>Searching</h2>
 <img src="https://github.com/lucasmargui/React_Estrutura_Search-Table/assets/157809964/a20faa3a-1c67-431f-80a5-3c0516f998ef" style="width:100%">

 </div>

## Project creation Next

```
npx create-next-app@latest nextjs-search
```

### Adding packages

```
npm i @heroicons/react
npm i clsx
npm i use-debounce
```

### Changing moduleResolution

Changing module to node resolution in tsconfig.json

```
...
"moduleResolution": "node",
...
```


# src\app directory

## home
 Directory where the components related to this page will be stored and has the path https://localhost:3000/home



![image](https://github.com/lucasmargui/React_Estrutura_Search-Table/assets/157809964/915357f7-819a-4a2f-9e37-608d35071814)


```
import { useDebouncedCallback } from 'use-debounce';:
```
- Imports the useDebouncedCallback function from a library called use-debounce. This function is used to create debounced callbacks that only run after a certain amount of inactivity.

```
export default function Search({ placeholder }: { placeholder: string }) {:
```

- Defines a function component called Search, which accepts a property called placeholder as a string.

```
const searchParams = useSearchParams();:
```

- Uses a hook called useSearchParams to obtain the URL search parameters.

```
const pathname = usePathname();:
```

- Uses a hook called usePathname to obtain the current path of the URL.

```
const { replace } = useRouter();:
```

- Uses a hook called useRouter to obtain a replace function that can be used to replace the current URL.

```
 const handleSearch = useDebouncedCallback((term) => { ... }, 300);:
```

- Creates a debounced callback called handleSearch that fires after 300 milliseconds of inactivity. This callback is responsible for updating the search parameters in the URL and replacing the current URL.


### Component ui/home/Table.tsx

![image](https://github.com/lucasmargui/React_Estrutura_Search-Table/assets/157809964/ccdeb3ac-c4e8-47de-a118-2b93371805f5)





