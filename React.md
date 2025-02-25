## Componentes
São blocos independentes e reutilizaveis podendo conter logicas diferentes.

## Tipos de componentes

**Function components-** mais novo - usam Hooks para lidar com estado
 **Componentes de Classe (Class Components)** - Antigo

## Comunicação entre Componentes
-   **Pai para filho:** Passando `props`.
-   **Filho para pai:** Usando callbacks.
-   **Entre componentes independentes:** Context API, Redux ou eventos globais.

## Props
- Props são dados imutaveis passados de componente pai para componente filho
- são somente para leitura e não podem ser editados dentro do componente filho
- um props só pode ser alterado através do componente pai utilizando state e enviando novamente ao componente filho
## State
- Guarda informações internas do componente
- pode ser mudado através do useState()
- Re-renderiza quando o valor é alterado

# useCallback
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTIyNjY0MDk0MywtODExNjI1OTkwLC0xMD
c4NzI2M119
-->