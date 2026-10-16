# Pousada do Porto — implantação na Vercel

Projeto original TanStack Start/React com a hero atualizada para a fotografia enviada. Mantivemos o layout e os conteúdos.

## Publicação

1. Envie os arquivos deste ZIP (conteúdo da pasta, não o ZIP como um único arquivo) para um repositório privado no GitHub.
2. Na Vercel, clique em **Add New → Project → Import Git Repository** e escolha esse repositório.
3. Confira o **Framework Preset: TanStack Start** e a pasta raiz do projeto. O comando de build deve ser `npm run build`.
4. Publique. A Vercel fornecerá um endereço temporário para testar.
5. Em **Project → Settings → Domains**, adicione `pousadadoporto.ursolabs.com.br`.
6. No provedor DNS do domínio `ursolabs.com.br`, crie/atualize um **CNAME** com Host `pousadadoporto` e Valor **exatamente o destino que a Vercel informar** nessa tela (varia conforme configuração). Não altere os registros dos outros subdomínios.
7. Aguarde a validação e certificado TLS, confira HTTPS e todas as seções do site.

## Dependência importante — fotografias

O ZIP exportado pelo Lovable contém apenas metadados das 10 imagens internas (9 fotos e o logotipo), não seus arquivos binários. Para não quebrar os links durante a migração, esses metadados agora apontam para as URLs absolutas da aplicação original `pousadadoporto.lovable.app`. **Isso significa que a galeria e o logo ainda dependem do servidor original.** Não retire o projeto Lovable do ar até obter os arquivos reais e substituí-los localmente. Essas URLs não puderam ser testadas nesta sessão.

A foto da hero (`public/hero-pousada-do-porto.png`) e o favicon estão incluídos fisicamente neste ZIP.

## Google Maps

O Google Maps incorporado usa `VITE_LOVABLE_CONNECTOR_GOOGLE_MAPS_BROWSER_KEY` fornecido pelo ambiente original. Esse valor está no `.env` exportado e pode não estar autorizado para o novo domínio. Recomenda-se configurar a chave própria no painel **Settings → Environment Variables** da Vercel e liberar o domínio no Google Cloud. Se não funcionar, o site mostra o fallback de localização.

## Testes

Não foi possível executar `npm install` e `npm run build` neste ambiente porque a resolução de DNS para o npm registry está indisponível. A configuração foi feita com base nas instruções oficiais do TanStack Start/Vercel; o build e a versão publicada precisam ser verificados na Vercel.
