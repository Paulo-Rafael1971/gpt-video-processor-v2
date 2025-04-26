# GPT Video Processor

Este projeto é uma API serverless que recebe uma URL de vídeo do YouTube, baixa o vídeo usando `yt-dlp`, faz o upload para um bucket do S3 e retorna uma URL temporária para o vídeo.

## Estrutura do Projeto

- **api/analyze.py**: Função que lida com o download do vídeo e o upload para o S3.
- **vercel.json**: Arquivo de configuração da Vercel.
- **requirements.txt**: Dependências do projeto.
- **README.md**: Documentação do projeto.

## Como Rodar

1. Faça o deploy na Vercel.
2. Acesse a API usando o endpoint `/api/analyze`.
3. Envie a URL do vídeo do YouTube no corpo da requisição.

Exemplo de corpo de requisição:
```json
{
  "video_url": "https://www.youtube.com/watch?v=ID_DO_VIDEO"
}
```

## Dependências

- **yt-dlp**: Para fazer o download dos vídeos.
- **boto3**: Para interagir com o AWS S3.