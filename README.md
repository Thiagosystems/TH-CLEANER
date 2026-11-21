<p align="center">
  <img src="docs/logo.png" alt="TH Cleaner" width="220">
</p>

<h1 align="center">TH Cleaner</h1>

<p align="center">
  Limpador de disco e desinstalador completo para Windows, com remoção de sobras e backup do registro.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Windows-10%20%7C%2011-0078D6?logo=windows" alt="Windows">
  <img src="https://img.shields.io/badge/.NET-8-512BD4?logo=dotnet" alt=".NET 8">
  <img src="https://img.shields.io/badge/licen%C3%A7a-MIT-green" alt="Licença MIT">
</p>

---

## ✨ Recursos

### 🧹 Limpeza de disco
- **Windows**: temporários do usuário e do sistema, Lixeira, cache de miniaturas, cache do Windows Update, Otimização de Entrega, relatórios de erro, despejos de memória, logs antigos, cache de shaders, Prefetch, arquivos recentes e cache DNS
- **Navegadores**: Chrome, Edge, Brave, Vivaldi, Opera, Opera GX e Firefox (cache, cookies e histórico, separados), com todos os perfis
- **Aplicativos**: Discord, Spotify, Steam, Epic Games, Teams, VS Code e caches de desenvolvedor (npm, pip, NuGet)
- **Analisar antes de limpar**: mostra quanto cada item ocupa
- Só aparecem os navegadores e apps instalados no PC
- Avisos nos itens que podem ter efeito colateral (ex.: cookies deslogam dos sites)
- Opção de fechar navegadores e apps abertos automaticamente
- Temporários só são apagados depois de X horas (configurável)
- **Lista de exclusões**: pastas que nunca serão apagadas
- Arquivos em uso são ignorados com segurança

### 📦 Arquivos grandes
- Procura em qualquer pasta ou disco os arquivos acima de 50 MB a 10 GB
- Filtro por tipo: vídeos, instaladores/ISO, compactados, imagens/áudio
- Abrir o local do arquivo, marcar vários e excluir (para a Lixeira ou de vez)

### 🗑️ Desinstalador completo
- Lista todos os programas instalados com ícone, fabricante, versão, data e tamanho
- Pesquisa e ordenação por nome, tamanho, data ou fabricante
- **Desinstalação + varredura de sobras**: depois do desinstalador, procura pastas, atalhos e chaves do registro que ficaram para trás
- **Remoção forçada** para programas com desinstalador quebrado
- **Desinstalação em lote**: marque vários e eles são removidos em sequência
- Desinstalação silenciosa quando o programa permite
- Itens com nome igual ao do programa já vêm marcados; os parecidos ficam para você decidir
- Proteções: nunca apaga pastas do sistema e não marca nada automaticamente se outro programa tiver o mesmo nome ou usar a mesma pasta
- Abrir a pasta de instalação, abrir a chave no Editor do Registro ou pesquisar o programa na web
- Exportar a lista de programas em CSV ou TXT

### 🛍️ Apps da Microsoft Store
- Lista os apps da Store e os pré-instalados do Windows
- Remove um ou vários de uma vez (os protegidos pelo sistema aparecem desativados)

### 🛡️ Segurança
- **Ponto de restauração** antes de desinstalar (opcional)
- **Backup do registro** antes de apagar qualquer chave, com restauração em um clique
- Pastas de sobras vão para a **Lixeira** (opcional)

### 🎨 Personalização
- Temas escuro, preto (AMOLED) e claro
- 8 combinações de cores prontas ou cores próprias
- Cor da logo ajustável

## 📥 Download

Baixe a versão mais recente na aba [**Releases**](https://github.com/Thiagosystems/THCleaner/releases).

> Requer o [.NET 8 Desktop Runtime](https://dotnet.microsoft.com/download/dotnet/8.0) (x64).
> O programa pede permissão de **administrador**, que é necessária para limpar pastas do sistema e desinstalar programas.

## 🛠️ Compilar

Pré-requisito: [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)

```bat
git clone https://github.com/Thiagosystems/THCleaner.git
cd THCleaner
build.bat
```

O executável fica em `publish\THCleaner.exe`.

## 📁 Estrutura

| Arquivo | Função |
|---|---|
| `DiskCleaner.cs` | Categorias de limpeza, análise e limpeza |
| `LargeFiles.cs` | Busca de arquivos grandes |
| `Uninstaller.cs` | Programas, desinstalação, sobras, backups e apps da Store |
| `Util.cs` | Lixeira, comandos e utilidades |
| `ThemeManager.cs` | Temas e cores |
| `AppSettings.cs` | Configurações (`%AppData%\THCleaner\settings.json`) |
| `MainWindow.xaml` | Interface |

## ❓ Perguntas frequentes

**Alguns arquivos não foram apagados. É normal?**
Sim. Arquivos em uso pelo Windows ou por programas abertos são mantidos, e o TH Cleaner mostra quantos foram ignorados.

**Removi algo do registro sem querer. Como volto?**
Vá em **Backups** e clique em **Restaurar**. Para casos maiores, use o ponto de restauração do Windows criado antes da desinstalação.

**Onde ficam os backups?**
Em `%AppData%\THCleaner\Backups`.

## 📄 Licença

Distribuído sob a licença MIT. Veja [LICENSE](LICENSE).
