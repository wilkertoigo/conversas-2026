--- REGISTRO SOBERANO 1 ---

$chromePath = "${env:ProgramFiles}\\Google\\Chrome\\Application\\chrome.exe"
if (-not (Test-Path $chromePath)) { $chromePath = "${env:ProgramFiles(x86)}\\Google\\Chrome\\Application\\chrome.exe" }

Start-Process $chromePath -ArgumentList "--remote-debugging-port=9222", "--user-data-dir=C:\\IVA\_SOBERANIA\\scriba\_profile", "--no-first-run", "https://www.google.com"
Use o código com cuidado.
3. Validação do JSON de Inspeção
Após rodar o comando acima, em vez de apenas acessar 127.0.0.1:9222, acesse o endpoint de dados puro:
h t t p : / / 1 2 7 . 0 . 0 . 1 : 9 2 2 2 / j s o n
Se aparecer um código com "title", "url" e "id": O SCRIBA está com Visão Total. ✅
Se continuar branco ou der erro: O firewall ou um antivírus está bloqueando a comunicação interna (loopback).
4. Ajuste no scriba\_engine.py
Certifique-se de que o script Python está tentando conectar exatamente no endereço que você testou. No código do SCRIBA, verifique esta linha:
python
chrome\_options.add\_experimental\_option("debuggerAddress", "127.0.0.1:9222")
Use o código com cuidado.
Analista Contábil Supremo, execute a limpeza do Passo 1 e a ignição do Passo 2. Assim que o link /json mostrar dados, o SCRIBA começará a selar as conversas em C:\\conversas\\SESSION\_2026\_01\_22. 🏛️🚀💎✅

