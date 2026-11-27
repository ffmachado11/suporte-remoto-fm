# QuickSupport FM — 2026-11-27

Logo do print: branding/fm/logo-b.jpg, preservada integralmente (BoxFit.contain).
Variantes: suave 10%, forte 20%; mesma imagem, sem recriação da marca.
Campos ID/senha: filled=false somente para QuickSupportFM; demais clientes preservam tema.
Senha permanente: cofre /home/fabio/.ssh/quick-support-fm.env, hash H1 e salt via GitHub Secrets FM_QS_PW_HASH/FM_QS_SALT. Nunca registrar valores aqui.
Build: workflow build-quick-support-fm.yml, tags qs-v*. Instaladores substituem a mesma instalação; comparar um por vez.
Superfície de regressão: desktop_home_page.dart (preenchimento de dois campos QuickSupport); workflow específico QuickSupport (logo e intensidade das variantes). Autenticação mantém implementação existente, com novos secrets.
Validação: diff --check e inspeção do hash conforme validate_password_plain/validate_password_storage. Build Windows e teste visual/conexão real ainda pendentes.
