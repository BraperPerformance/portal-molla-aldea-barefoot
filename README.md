# Aldea Barefoot · Central do Cliente (Molla)

Portal estático com tela de acesso e apresentação do diagnóstico e plano de mídia paga.

## Estrutura
- `index.html` — tela de login (nome livre + senha)
- `apresentacao.html` — deck em HTML (só abre após o login)
- `assets/` — logos Molla e Aldea
- `vercel.json` — URLs limpas e noindex

## Publicar
1. Crie um repositório no GitHub e envie estes arquivos.
2. No Vercel, importe o repositório (framework: Other, sem build). Deploy.
3. Acesse a URL gerada. A senha fica registrada como hash SHA-256 no `index.html`.

## Trocar a senha
Gere o SHA-256 da nova senha e substitua o valor de `HASH` no `index.html`.
Ex.: `echo -n "NOVASENHA" | shasum -a 256`

Observação: a proteção é feita no navegador (sessionStorage). Serve para restringir o acesso casual ao link, não substitui autenticação de servidor.
