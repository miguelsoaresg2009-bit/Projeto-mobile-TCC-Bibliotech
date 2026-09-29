# BiblioTech Mobile (Expo / React Native)

Versão beta em desenvolvimento do projeto de TCC do terceiro semestre.

Aplicativo móvel de biblioteca escolar que ajuda alunos a encontrar livros e outros materiais
para leitura, pesquisa e estudo. O BiblioTech reúne o acesso ao acervo em uma experiência
pensada para apoiar a rotina de estudos.

App mobile do BiblioTech: mesma lógica do `front_react_v2`, consumindo a mesma API Spring Boot
(`back/bibliotecadigital`) e o banco SQL Server (`bibliotecadigital_sqlserver.sql`).

## Como rodar
1. Suba o SQL Server, rode o script `.sql` e ligue o back-end (porta 8080).
2. Descubra o IP do PC (`ipconfig` -> Endereço IPv4) e ponha em `src/config.jsx`.
3. Libere a porta 8080 no Firewall do Windows (rede privada) se o celular não conectar.
4. Nesta pasta:
   ```bash
   npm install
   npx expo start
   ```
5. Abra o app **Expo Go** no celular (mesmo Wi-Fi do PC) e leia o QR Code.

Logins de teste: `admin` / `admin123` (Painel Administrativo) e `aluno1` / `123456` (Portal do Aluno).

## Diferenças em relação ao React web
- Sem upload de capa de livro (usa a capa genérica ou a que já existir no servidor).
- Navegação por barra de abas inferior (mesma lógica de estado do `App.jsx`).
- Modo escuro e login ficam só na memória (igual ao React, que também perde o login ao recarregar).
- Se o servidor devolver 401 (ex.: back reiniciado), o app volta sozinho para o login.
