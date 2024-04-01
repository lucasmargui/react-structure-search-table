

<H1 align="center">Estrutura Next Search </H1>
<p align="center">🚀Criação de uma estrutura de search em Next para referências futuras</p>


## Criação de projeto Next

```
npx create-next-app@latest nextjs-search
```

### Adicionando pacotes 

```
npm i @heroicons/react
npm i clsx
npm i use-debounce
```

### Alterando moduleResolution

Alteração da resolução de módulo para node em tsconfig.json

```
...
"moduleResolution": "node",
...
```


# Diretório src\app

## home
  Diretório onde armazenará os componentes relacionados a está página e tem como caminho https://localhost:3000/home

  

![image](https://github.com/lucasmargui/React_Estrutura_Search-Table/assets/157809964/915357f7-819a-4a2f-9e37-608d35071814)


```
import { useDebouncedCallback } from 'use-debounce';:
```
- Importa a função useDebouncedCallback de uma biblioteca chamada use-debounce. Essa função é usada para criar callbacks debounced (adiados) que só são executados após um certo tempo de inatividade.

```
export default function Search({ placeholder }: { placeholder: string }) {:
```

- Define um componente de função chamado Search, que aceita uma propriedade chamada placeholder como uma string.

```
const searchParams = useSearchParams();:
```

- Utiliza um hook chamado useSearchParams para obter os parâmetros de pesquisa da URL.

```
const pathname = usePathname();:
```

-  Utiliza um hook chamado usePathname para obter o caminho atual da URL.

```
const { replace } = useRouter();:
```

- Utiliza um hook chamado useRouter para obter uma função replace que pode ser usada para substituir a URL atual.

```
 const handleSearch = useDebouncedCallback((term) => { ... }, 300);:
```

- Cria um callback debounced chamado handleSearch que é acionado após 300 milissegundos de inatividade. Este callback é responsável por atualizar os parâmetros de pesquisa na URL e substituir a URL atual.





