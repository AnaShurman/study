## Domain Drive Design (DDD)
- design orientado ao dominio
- é uma abordagem que foca em entender profundamente o problema real que o software vai resolver 
- O objetivo é alinhar **software, linguagem e regras de negócio**, para que o sistema reflita a realidade do usuário.

## vantagens:
 - evita sistemas bagunçados
 - alinha devs e especialista do negocio
 - facilita manutenção de codigo
 - deixa o sistema mais organizado

## Design estrategico
é importante identificar o dominio, o core daquele projeto
Dominio pode ser separado em:
- subdominio principal: é o que te diferencia dos outros no mercado, vc pode ter mais de 1 sub dominio principal
- subdominio generico: conjunto de processos comuns no mercado, ex financeiro. todas as empresas tem
- subdominio suporte: apoia o negocio da empresa mas não da nenhuma vantagem estrategica
usando essa analise conseguimos seguir estrategias que de adaptem melhor projeto
- priorizar o core primeiro 

## Domain Storytelling
- utiliza linguagem Pictográfica
- possibilita observar o quão conectado estão as coisas dentro do processo para identificar possiveis impactos.
contem:
	- atores
	- objetivos de trabalho
	- atividades 
	- fluxo da historia
	- anotações
	- grupos
	- cores
- no storytelling é necessario detalhar cada uma das ações do projeto
- buscar sempre responder (como, onde, por que, pra quem )
- separar em diferentes cenarios para não deixar um unico diagrama complexo

### como definir o escopo
existem 5 niveis de detalhamento de escopo, normalmente ficamos no nivel 3 de detalhamento onde temos uma visão clara dos processos Principais mas sem precisar de um nivel de detalhamento tão grande.

- identificar se o usuario esta falando do processo que ela ja faz ou do processo que ela gostaria de fazer; 
- dominio puro: mostramos apenas as interações entre os atores sem ressaltar a tecnologia sendo utilizada;
- dominio digitalizado: mostramos as interações entre os atores e a tecnologia sendo utilizada;

### Linguagem Ubíqua
- É uma **linguagem comum e compartilhada** entre todos os envolvidos no projeto;
###  Modelagem de Domínio
- é importante entender como as coisas se relacionam entre si;

**ferramentas**
- Wiki
- repositorios
- gestão de processo

### Contexto Delimitado
É a **fronteira clara** onde **um modelo de domínio específico** se aplica e **tem significado consistente**.
> Ou seja: **dentro de um contexto delimitado, os termos da linguagem ubíqua são bem definidos e não mudam de sentido**.

- cada dominio deve ter seus proprios conceitos delimitados separadamente, ex: ( marketing e o financeiro)

### Kernel compartilhado
- quando dois times diferentes tem informações compartilhadas entre si, o que acada ultrapassando o contexto delimitado é importante discutir entre ambas as equipes para criar uma linguagem ubiqua entre ambos, evitando assim mal entendidos e deixando todas as pessoas com a mesma visão do processo
- evite ao maximo compartilhar o mesmo codigo em dois times diferentes pois a chance de conflitos é muito grande.
- quando a aplicação realmente depender de fluxos que impactem ampas os setores, criar uma terceira aplicação que faça exclusivamente esse processo é uma boa opção, evitando que as aplicações principais acabem conflitando
-  
### Modelo cliente - fornecedor
- nesse modelo os times trabalham de forma separada porém eles contem uma dependencia por conta de um serviço, por exemplo usar serviços de autentificação do google.
- quando um fornecedor vai e muda a estrutura do serviço e o sistema cliente tem que adaptar a forma que ele utiliza, se denomina **conformista**

### Camada anti-corrupção (ACL)
- existe para proteger a aplicação de mudanças no serviço provido
- evita de corromper a camada core do codigo, é uma camada desenvolvida antes e fora do codigo principal pois se for necessario fazer manipulações vc mexe exclusivamente nela ao inves de no resto do codigo.

- **Keycloak** :  é uma **ferramenta open-source de identidade e acesso** (IAM - _Identity and Access Management_), que cuida de:
✅ Autenticação (Login)  
✅ Autorização (Permissões)  
✅ SSO (Single Sign-On)  
✅ OAuth2, OpenID Connect, SAML  
✅ Gerenciamento de usuários, papéis e grupos  
✅ Login social (Google, Facebook, etc.)

##	Open host service
Um **Open Host Service** é:
-   Uma **interface pública bem definida** (como uma API REST, GraphQL, gRPC, eventos Kafka, etc.)  
-  Exposta **por um contexto delimitado**
-   Para que **outros sistemas/contexts possam interagir com ele**
-   Sem acoplar diretamente ao **modelo interno ou estrutura de código**

### Linguagem publicada (PL)
- o fornecedor cria instancias de seu serviço custominadas
são empresas que fazem o ACL por vc : 
- Neogrid
- nexxera
- accesstage
- informatica

## Design tatico

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTEwNjI0OTQ2OCw3MjMxNzI3ODAsLTcwOT
AxODY4Myw1MjA4Njk4OSwtMTc4NDUzMDExNiwxNDI4Njk0ODA1
LDIwODgwMzM5NDgsMTYzMjM3MDI5NSwxNzk0OTc3NzAwLC03Mj
U1ODcyNjIsMTg5NzAyMzk1NCwtODAxNjc5Mjg3LC0xMzUzNDA4
MjA1LDIwODc0NDI1OTgsLTE0MzE0MjU1MjAsMjA4NzQ0MjU5OC
wxMzgxMzcwODUyLC0yNTg2NTQyOTYsMjEyMjY5NjYyNCwtMTc2
OTM3MTcxNF19
-->