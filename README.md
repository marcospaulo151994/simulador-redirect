# simulador-redirect

Redirecionamento de `simulador.rafano.com.br` para o simulador de consórcio (Google Apps Script), servido via GitHub Pages.

Fluxo: CNAME no Registro.br (`simulador` → GitHub Pages) → o Pages serve este `index.html` → meta refresh + `location.replace` levam à URL `/exec` da implantação.

A implantação ainda não existe: depois de implantar o web app, substitua **todas** as ocorrências de `SUBSTITUIR_URL_EXEC_AQUI` no `index.html` pela URL `/exec`. Ela permanece estável desde que as reimplantações usem sempre o mesmo deployment (`npx clasp deploy -i <ID>`).

O acesso ao simulador continua protegido pelo login do Google Workspace — este repositório só encurta o endereço.
