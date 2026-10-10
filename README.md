# SysLink

SysLink é um utilitário nativo de desktop moderno, ultraleve e de alto desempenho desenvolvido pela **MProgram Corp.** com o objetivo de gerenciar visualmente, criar e realizar migrações transparentes de **Junções de Diretório (NTFS Junctions)** e **Links Simbólicos (Symlinks)** no Windows. Permitindo liberar espaço em discos primários e SSDs ao transferir pastas volumosas (jogos, bibliotecas, máquinas virtuais e caches) para outras unidades sem quebrar o sistema operacional ou caminhos de aplicativos.

---

## Pré-requisitos

- **Sistema Operacional**: Windows 10 ou Windows 11 (64-bit recomendados). *(Obs: Em outras versões do Windows, o SysLink não foi testado!)*
- **Sistema de Arquivos**: NTFS (necessário para suporte a Reparse Points, Junções e Links Simbólicos).
- **Permissões**: O aplicativo roda como processo de usuário comum, sem necessidade de privilégios de Administrador.

O SysLink é um executável nativo em C++20 com pipeline gráfico DirectX 11 dedicado e alocador de memória de alta performance *Segment Heap*, livre de dependências pesadas e pronto para uso imediato sem necessidade de instalador.

---

## Funcionalidades

### Interface e Experiência do Usuário (UI/UX)
- **Arrastar e Soltar (Drag & Drop)**: Arraste pastas diretamente do Windows Explorer para dentro da janela do aplicativo para preencher automaticamente os campos de origem e identificação.

### Assistente de Migração
- **Migração Transparente e Segura**: Copia integralmente o conteúdo da pasta pesada para o disco secundário e substitui a pasta original por uma junção NTFS idêntica.
- **Validação e Varredura**: Contagem precisa de arquivos, subpastas e tamanho total, com checagem em tempo real de espaço livre no disco de destino e margem de segurança.
- **Detecção de Processos Bloqueantes**: Integração nativa com a *Windows Restart Manager API* para identificar e listar programas abertos que estejam bloqueando arquivos na pasta antes de iniciar a migração.
- **Motor de Cópia com Rollback Automático**: Cópia byte-a-byte. Em caso de cancelamento pelo usuário ou falha de disco, o sistema reverte as alterações automaticamente, restaurando os dados com total integridade.

### Gerenciador Central de Vínculos (Banco de Links)
- **Monitoramento Contínuo de Saúde**: Varredura automática ao iniciar para diagnosticar o estado de cada link no sistema de arquivos (`[OK] Íntegro`, `[!] Ausente`, `[X] Rompido`).
- **Navegação e Ações Rápidas**: Botões dedicados para abrir instantaneamente o local de **Origem** no Explorer, a pasta real de **Destino** ou iniciar a **Desvinculação**.
- **Assistente de Desvinculação Segura (Safe Unlink)**: Escolha flexível entre remover apenas o vínculo NTFS (mantendo todos os arquivos no destino) ou retornar todos os arquivos para a pasta de origem original antes de remover a junção.
- **Busca e Filtros Instantâneos**: Localize vínculos rapidamente por nome, tipo de link ou filtre apenas vínculos que apresentem alertas de integridade.

### Armazenamento Persistente e Shell do Windows
- **Persistência Transparente no Perfil do Usuário**: Salva o histórico de links e configurações em `%LocalAppData%\SysLink\storage\links.json`, mantendo rotação automática dos últimos 20 backups diários na subpasta `backups/`.
- **Menu de Contexto do Windows Explorer**: Ativação com um clique no painel de configurações para registrar a opção **"Mover e Criar Link com SysLink"** diretamente no botão direito do Windows Explorer.

---

## Como usar

1. Faça o download do [SysLink v1.0.0](https://github.com/MProgramCorp/SysLink/releases/tag/v1.0.0) (versão mais recente).
2. Execute o arquivo `SysLink.exe` (não requer instalação).
3. Na aba **Novo Link & Migração**:
   - Arraste ou selecione a pasta de origem que deseja mover (ex: `C:\Jogos\JogoPesado`).
   - Selecione a pasta de destino no disco com espaço livre (ex: `D:\Migracoes\JogoPesado`).
   - Clique em **Iniciar Migração**.
4. Acompanhe a barra de progresso em tempo real até a conclusão. O jogo ou aplicativo continuará acessível pelo caminho original sem ocupar espaço no disco primário.
5. Acesse a aba **Banco de Links** a qualquer momento para auditar a integridade dos seus vínculos ou desfazê-los com segurança.

---

## Contribuição

Contribuições para o projeto são sempre bem-vindas! Se você tiver alguma sugestão, melhoria ou encontrar algum problema:
1. Abra uma **Issue** relatando o caso ou propondo uma nova ferramenta.
2. Envie um **Pull Request** com suas alterações.

---

## Contato

- **Suporte**: [suporte@mprogram.com.br](mailto:suporte@mprogram.com.br)
- **Sugestões e Contato Geral**: [contato@mprogram.com.br](mailto:contato@mprogram.com.br)
- **Organização GitHub**: [MProgramCorp](https://github.com/MProgramCorp)

---

## Licença

Veja o arquivo [LICENSE.md](LICENSE.md) para os termos de uso do software.

## Notas de Lançamento

Veja o arquivo [RELEASES.md](RELEASES.md) para o histórico completo de versões e notas de lançamento do SysLink.

---

Agradecemos pelo seu apoio contínuo ao **SysLink**. Estamos comprometidos em oferecer a melhor experiência possível. Entre em contato conosco para sugestões ou feedback.
