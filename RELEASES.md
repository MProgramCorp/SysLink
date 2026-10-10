# Releases

## [Versão 1.0.0](https://github.com/MProgramCorp/SysLink/releases/tag/v1.0.0)
*Versão mais recente do SysLink*

### Interface (UI/UX)

- **Arrastar e Soltar (Drag & Drop)**: Suporte completo para arrastar pastas de qualquer janela do Windows Explorer diretamente para o assistente de migração.

### Motor de Migração e Vínculos NTFS

- **Migração Transparente**: Transferência segura de pastas pesadas para unidades secundárias substituindo o caminho original por um ponto de junção NTFS de forma transparente para o Windows.
- **Motor de Cópia com Rollback Automático**: Cópia byte-a-byte e reversão de arquivos em caso de cancelamento ou falha.
- **Persistência Transparente em %LocalAppData%**: Banco de dados seguro gravado atomicamente em disco com cópias de segurança automáticas e rotação dos últimos 20 backups diários.

## Funcionalidades:

- **Migração Transparente de Pastas**: Transfira jogos e pastas pesadas para outros discos sem quebrar atalhos ou programas.
- **Junções de Diretório (NTFS Junctions)**: Criação de vínculos em baixo nível no sistema de arquivos NTFS.
- **Links Simbólicos (Symlinks)**: Suporte nativo para criação de links simbólicos de diretórios.
- **Rollback**: Restauração integral dos dados caso a transferência seja cancelada pelo usuário ou interrompida.
- **Banco de Links Central**: Monitoramento e diagnóstico contínuo de saúde dos links (`[OK] Íntegro`, `[!] Ausente`, `[X] Rompido`).
- **Desvinculação Segura (Safe Unlink)**: Assistente para remover apenas o vínculo ou mover os arquivos de volta para a origem original.
- **Armazenamento no Perfil do Usuário**: Gravação limpa em `%LocalAppData%\SysLink\storage\links.json` sem necessidade de banco de dados externo.
- **Menu de Contexto do Windows**: Integração limpa no Registro para mover pastas clicando com o botão direito no Windows Explorer.

Agradecemos pelo seu apoio contínuo ao SysLink. Sua opinião é fundamental para nós. Se você tiver alguma dúvida, sugestão ou encontrar algum problema nesta versão, entre em contato ou abra uma issue no repositório. Estamos empenhados em proporcionar a melhor experiência possível aos nossos usuários.
