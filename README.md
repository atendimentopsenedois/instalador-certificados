# Instalador de Cadeias de Certificados

Instalador de cadeias de autoridades certificadoras (CA) para Windows 10/11 64 bits.

**Versão:** 1.0.0 (18/11/2026).

**[Baixar versão mais recente](https://github.com/atendimentopsenedois/instalador-certificados/releases/latest)**

O executável oferece interface gráfica, instalação em lote de certificados intermediários e confirmação separada para novas autoridades raiz. Não instala certificados pessoais A1/A3, não modifica configurações de TLS e não executa arquivos `.reg`.

**Atenção:** o executável ainda não possui assinatura digital de editor e não foi testado em um Windows real. Verifique a origem dos certificados antes de conceder confiança. A importação de uma cadeia não garante autenticidade ou ausência de revogação.

## Distribuição

As 16 partes codificadas em Base64 da versão 1.0.0 estão em `parts/`. Um fluxo de GitHub Actions remonta o executável original, confere o SHA-256 esperado e o disponibiliza como ativo da Release.

**SHA-256 esperado:** `B116511539A67EF9619BD03A7EE3B55B51583B4358D2C8071608558FCC6B689B`

Para atualizações futuras, substitua as partes e altere a versão, o SHA-256 e o fluxo de publicação antes de realizar novo release.
