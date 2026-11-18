# Instalador de Cadeias de Certificados

Instalador de cadeias de autoridades certificadoras (CA) para Windows 10/11 64 bits.

**Versao atual: 1.1.0 (18/11/2026).**

**[Baixar a versao mais recente](https://github.com/atendimentopsenedois/instalador-certificados/releases/latest)**

## Funcionalidades
- Importacao em lote de cadeias de certificados intermediarios e raizes selecionadas.
- Instalacao nos repositorios do usuario atual e da maquina local (com autorizacao administrativa quando necessaria).
- 162 certificados elegiveis incluidos no pacote (certificados vencidos excluidos na preparacao).
- Verificacao de validade na execucao, deteccao de duplicidades por repositorio e relatorio por destino.
- Novas autoridades raiz exigem autorizacao explicita.
- Nao instala certificados pessoais A1/A3, nao modifica TLS, nao executa arquivos .reg e nao requer acesso a Internet.

## Versoes e publicacao automatizada
- [v1.1.0](https://github.com/atendimentopsenedois/instalador-certificados/releases/tag/v1.1.0): atualizacao para usuario atual + maquina local, testada com sucesso pelo usuario em Windows.
- [v1.0.0](https://github.com/atendimentopsenedois/instalador-certificados/releases/tag/v1.0.0): primeira versao.

A v1.0.0 e reconstruida a partir de `parts/` pelo workflow `.github/workflows/publicar-instalador.yml`. A v1.1.0 utiliza os cinco arquivos de diferencas em `updates/v1.1.0/`, aplica o patch sobre a v1.0.0 validada e confere o SHA-256 final antes de publicar uma nova Release.

**SHA-256 v1.1.0:** `8fbb0398e2e841d596e9626c0d8b6cd583dd0f5401b27a47080099e5fc8d006f`.

**Seguranca:** o executavel ainda nao possui assinatura digital de editor. Certificados de autoridades raiz so devem receber confianca quando sua procedencia for confirmada. A importacao de uma cadeia nao comprova por si so ausencia de revogacao nem legitimidade do certificado.
