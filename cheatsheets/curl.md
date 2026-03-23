# =========================
# CURL CHEATSHEET PRÁTICO
# =========================

# -------------------------------------------------
# 1. REQUISIÇÕES BÁSICAS
# -------------------------------------------------

# Faz um GET simples e mostra o conteúdo da resposta
curl http://example.com

# Faz GET seguindo redirecionamentos
curl -L http://example.com

# Mostra apenas os headers da resposta
curl -I http://example.com

# Faz download salvando com o nome original do arquivo remoto
curl -O http://example.com/file.txt

# Faz download salvando com nome customizado
curl http://example.com/file.txt -o meu_arquivo.txt


# -------------------------------------------------
# 2. DIFERENÇA ENTRE -O e -o
# -------------------------------------------------

# -O (maiúsculo)
# Salva com o MESMO nome do arquivo remoto
curl -O http://site.com/arquivo.zip
# salva como: arquivo.zip

# -o (minúsculo)
# Salva com o nome que VOCÊ escolher
curl http://site.com/arquivo.zip -o backup.zip
# salva como: backup.zip


# -------------------------------------------------
# 3. HEADERS
# -------------------------------------------------

# -I
# Faz uma requisição HEAD: mostra só os headers
curl -I http://example.com

# Mostra headers da resposta junto com o body
curl -i http://example.com

# Adiciona header customizado
curl -H "Authorization: Bearer TOKEN" http://example.com

# Adiciona User-Agent customizado
curl -A "Mozilla/5.0" http://example.com


# -------------------------------------------------
# 4. MÉTODOS HTTP
# -------------------------------------------------

# GET explícito
curl -X GET http://example.com

# POST
curl -X POST http://example.com

# PUT
curl -X PUT http://example.com/1

# DELETE
curl -X DELETE http://example.com/1

# PATCH
curl -X PATCH http://example.com/1


# -------------------------------------------------
# 5. ENVIANDO DADOS
# -------------------------------------------------

# POST com form-data simples
curl -X POST -d "username=carlos&password=123" http://example.com/login

# POST com JSON
curl -X POST http://example.com/api \
  -H "Content-Type: application/json" \
  -d '{"name":"Carlos","role":"admin"}'

# PUT com JSON
curl -X PUT http://example.com/api/1 \
  -H "Content-Type: application/json" \
  -d '{"name":"Edu"}'


# -------------------------------------------------
# 6. AUTENTICAÇÃO
# -------------------------------------------------

# Basic Auth
curl -u usuario:senha http://example.com

# Bearer Token
curl -H "Authorization: Bearer TOKEN_AQUI" http://example.com/api

# Cookie manual
curl -H "Cookie: session=abc123" http://example.com

# Salvar cookies em arquivo
curl -c cookies.txt http://example.com

# Enviar cookies de arquivo
curl -b cookies.txt http://example.com

# Enviar cookie específico
curl -b "session=abc123" http://example.com


# -------------------------------------------------
# 7. DEBUG / ENUMERAÇÃO / ANÁLISE
# -------------------------------------------------

# Modo verbose: mostra detalhes da conexão e da requisição
curl -v http://example.com

# Mostra ainda mais detalhes (inclui tráfego bruto)
curl --trace - http://example.com

# Mostra status code ao final
curl -s -o /dev/null -w "%{http_code}\n" http://example.com

# Mostra IP remoto, status code e tipo de conteúdo
curl -s -o /dev/null -w "IP: %{remote_ip}\nCode: %{http_code}\nType: %{content_type}\n" http://example.com

# Ignora erro de certificado TLS/SSL
curl -k https://example.com

# Define timeout máximo
curl --max-time 10 http://example.com

# Define timeout de conexão
curl --connect-timeout 5 http://example.com


# -------------------------------------------------
# 8. REDIRECIONAMENTOS
# -------------------------------------------------

# Não segue redirecionamento
curl http://example.com

# Segue redirecionamento
curl -L http://example.com

# Ver só os headers e descobrir Location
curl -I http://example.com


# -------------------------------------------------
# 9. DOWNLOADS ÚTEIS
# -------------------------------------------------

# Download com nome original
curl -O http://example.com/file.txt

# Download com nome customizado
curl http://example.com/file.txt -o local.txt

# Continuar download interrompido
curl -C - -O http://example.com/file.zip

# Baixar vários arquivos
curl -O http://site.com/1.txt -O http://site.com/2.txt


# -------------------------------------------------
# 10. UPLOAD DE ARQUIVOS
# -------------------------------------------------

# Upload multipart/form-data
curl -X POST http://example.com/upload \
  -F "file=@arquivo.txt"

# Upload com campo adicional
curl -X POST http://example.com/upload \
  -F "file=@arquivo.txt" \
  -F "user=edu"


# -------------------------------------------------
# 11. APIs
# -------------------------------------------------

# GET em API com JSON
curl http://example.com/api/users \
  -H "Accept: application/json"

# POST JSON em API
curl -X POST http://example.com/api/users \
  -H "Content-Type: application/json" \
  -d '{"username":"edu","email":"edu@test.com"}'

# PUT JSON
curl -X PUT http://example.com/api/users/1 \
  -H "Content-Type: application/json" \
  -d '{"role":"admin"}'


# -------------------------------------------------
# 12. HTTPS / CERTIFICADOS
# -------------------------------------------------

# Ignora validação TLS
curl -k https://example.com

# Usa certificado cliente
curl --cert cert.pem --key key.pem https://example.com

# Especifica CA customizada
curl --cacert ca.pem https://example.com


# -------------------------------------------------
# 13. PROXY
# -------------------------------------------------

# Usar proxy HTTP
curl -x http://127.0.0.1:8080 http://example.com

# Útil com Burp Suite
curl -x http://127.0.0.1:8080 -k https://example.com


# -------------------------------------------------
# 14. OPÇÕES MUITO ÚTEIS PRA PENTEST / ESTUDO
# -------------------------------------------------

# Silencioso (não mostra barra de progresso)
curl -s http://example.com

# Silencioso, mas mostra erros
curl -sS http://example.com

# Salva body em arquivo e mostra status code
curl -s -o resposta.html -w "%{http_code}\n" http://example.com

# Testar endpoint com método específico
curl -X OPTIONS -i http://example.com/api

# Ver headers + body
curl -i http://example.com

# Fazer HEAD request
curl -I http://example.com

# Forçar resolução de host pro seu / laboratório
curl http://site.com --resolve site.com:80:10.10.10.10

# Ignorar certificado e usar proxy Burp
curl -k -x http://127.0.0.1:8080 https://target.com


# -------------------------------------------------
# 15. EXEMPLOS RÁPIDOS DO MUNDO REAL
# -------------------------------------------------

# Descobrir status code
curl -s -o /dev/null -w "%{http_code}\n" http://target.com/login

# Ver se existe redirecionamento
curl -I http://target.com

# Baixar arquivo encontrado numa enumeração
curl -O http://target.com/backups/db.sql

# Testar API com token
curl http://target.com/api/user \
  -H "Authorization: Bearer eyJ..."

# Enviar cookie de sessão
curl http://target.com/admin \
  -H "Cookie: PHPSESSID=abc123"

# Testar JSON em endpoint
curl -X POST http://target.com/api/login \
  -H "Content-Type: application/json" \
  -d '{"username":"carlos","password":"123456"}'

# Ver resposta completa passando por Burp
curl -v -x http://127.0.0.1:8080 -k https://target.com

# Resumo mental rápido

curl URL            # GET normal
curl -I URL         # só headers
curl -i URL         # headers + body
curl -O URL         # salva com nome original
curl -o arq URL     # salva com nome escolhido
curl -L URL         # segue redirect
curl -X POST URL    # define método
curl -d "a=1" URL   # envia dados
curl -H "k:v" URL   # adiciona header
curl -b cookie.txt  # envia cookies
curl -c cookie.txt  # salva cookies
curl -u user:pass   # basic auth
curl -k URL         # ignora TLS
curl -v URL         # verbose
curl -x proxy URL   # usa proxy

# O que decorar primeiro

# Pra uso real, eu decoraria estes:

-I   # só headers
-i   # headers + body
-O   # salvar com nome original
-o   # salvar com nome custom
-L   # seguir redirect
-H   # header custom
-X   # método HTTP
-d   # enviar dados
-b   # enviar cookie
-c   # salvar cookie
-v   # verbose
-k   # ignorar certificado
-s   # silencioso
-w   # formatar saída (status code etc.)