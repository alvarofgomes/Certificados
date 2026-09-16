# Meus Certificados Profissionais

Este repositório armazena uma coleção dos certificados que fui adquirindo e aprimorando ao longo da minha carreira como desenvolvedor Back-End. A cada nova fase profissional e conquista, novos certificados serão adicionados, representando minha evolução e habilidades adquiridas.

## Sobre Mim

Sou Alvaro Filipe, um desenvolvedor back-End com foco em criar Java, com uma forte base em Programação Orientada a Objetos (POO). Estou sempre buscando melhorar minhas habilidades para desenvolver soluções eficientes e escaláveis. 

## Sincronização automática com o portfólio

Este repositório é a fonte de verdade dos certificados exibidos em
[alvarofgomes.github.io/Portfolio_alvarofgomes](https://alvarofgomes.github.io/Portfolio_alvarofgomes/).
O arquivo [`certificados.json`](./certificados.json) lista, para cada PDF, o título em
PT/EN e a categoria. Ao dar push na `main`, um workflow (`.github/workflows/notify-portfolio.yml`)
avisa o repositório do portfólio, que busca este manifesto, regenera os dados e publica
o site sozinho — não precisa mexer em nada no outro repositório.

Os PDFs **não são copiados** para o portfólio: o site aponta direto para eles através do CDN
do jsDelivr (`https://cdn.jsdelivr.net/gh/alvarofgomes/Certificados@main/<arquivo>`). Ou seja,
este repositório é a única cópia dos arquivos.

### Como adicionar um certificado novo

1. Coloque o PDF na raiz deste repositório.
2. Adicione uma entrada em `certificados.json`:
   ```json
   {
     "arquivo": "Nome Exato Do Arquivo.pdf",
     "titulo_pt": "Título em português",
     "titulo_en": "Title in English",
     "categoria": "ia"
   }
   ```
   Categorias válidas: `java`, `web`, `git`, `ia`, `office`, `python`, `sql`, `outros`.
3. Commit + push na `main`. O site atualiza sozinho em alguns minutos.

> O campo `arquivo` precisa bater **exatamente** com o nome do PDF (acentos, espaços e
> maiúsculas incluídos). Se não bater, a sincronização falha avisando qual entrada está errada.

### Substituí um PDF mantendo o mesmo nome e o site mostra o antigo

O CDN guarda o arquivo em cache por um tempo. Para forçar a atualização imediata:

```bash
curl -X POST https://purge.jsdelivr.net/ \
  -H "Content-Type: application/json" \
  -d '{"path":["/gh/alvarofgomes/Certificados@main/NOME DO ARQUIVO.pdf"]}'
```

Isso só é necessário ao **substituir** um arquivo existente — certificados novos aparecem na hora.

## Como Utilizar

Sinta-se à vontade para explorar os arquivos neste repositório para conhecer melhor minha trajetória e competências.

## Contato

- LinkedIn: www.linkedin.com/in/alvarofgomes
- Portfólio: https://alvarofgomes.github.io/Portfolio_alvarofgomes/
- Email: [alvarogomes098@gmail.com](mailto:alvarogomes098@gmail.com)