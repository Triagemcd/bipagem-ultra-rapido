# 🚀 Sistema de Bipagem Ultra-Rápido

Sistema web de validação instantânea de códigos vs CEPs para operadores de bipagem, com performance < 100ms usando GitHub Pages + JSON.

## 📋 Características Principais

- ⚡ **Performance Ultra-Rápida**: Validação em menos de 100ms
- 💰 **Totalmente Gratuito**: Hospedado no GitHub Pages
- 🔧 **Zero Configuração**: Funciona apenas abrindo o link
- 📱 **Responsivo**: Desktop, tablet e mobile
- 🔍 **Compatível com Scanners**: Suporta leitores de código de barras
- 🌙 **Modo Noturno**: Automático baseado no horário
- 📊 **Estatísticas em Tempo Real**: Acompanhamento de performance
- 💾 **Logs Automáticos**: Histórico completo das operações

## 🚀 Como Usar (Operador)

1. **Acesse o sistema**: `https://[usuario].github.io/bipagem-ultra-rapido`
2. **Faça login** com sua matrícula e senha
3. **Configure o CEP** da gaiola que está processando
4. **Comece a bipar** - o sistema valida automaticamente

### Credenciais de Teste
- Matrícula: `1234` | Senha: `1234` (João Silva)
- Matrícula: `5678` | Senha: `5678` (Maria Santos)
- Matrícula: `9999` | Senha: `9999` (Carlos Oliveira)

## 🔧 Instalação (Administrador)

### 1. Fork este repositório
Clique no botão "Fork" no GitHub

### 2. Ative o GitHub Pages
1. Vá em Settings → Pages
2. Source: Deploy from a branch
3. Branch: main / (root)
4. Clique em Save

### 3. Acesse seu sistema
`https://[seu-usuario].github.io/bipagem-ultra-rapido`

## 📁 Estrutura dos Arquivos

```
bipagem-ultra-rapido/
├── index.html         # Sistema completo (standalone)
├── codigos.json      # Base de dados dos códigos
├── operadores.json   # Dados de login dos operadores
└── README.md         # Esta documentação
```

## 🔄 Atualização dos Dados

### Método Manual
1. Edite o arquivo `codigos.json` diretamente no GitHub
2. Commit as mudanças
3. O sistema detecta automaticamente (cache de 30 minutos)

### Método Automático (Recomendado)
Use GitHub Actions para sincronizar com Google Sheets:

1. Crie um Google Sheets com os códigos
2. Configure GitHub Actions para atualizar automaticamente
3. Os dados são sincronizados a cada hora

## 📊 Estrutura dos Dados

### codigos.json
```json
{
  "lastUpdate": "2025-07-15T10:30:00Z",
  "totalCodes": 1247,
  "codes": {
    "BR259747338411J": "36960000",
    "BR253223789688Z": "36950000"
  }
}
```

### operadores.json
```json
{
  "operators": {
    "1234": {
      "nome": "João Silva",
      "senha": "1234",
      "setor": "Expedição"
    }
  }
}
```

## ⚡ Performance

- **Carregamento inicial**: < 3 segundos
- **Validação de código**: < 100ms (cache local)
- **Zero chamadas de API** durante operação
- **Funciona offline** após carregamento inicial

## 🎯 Funcionalidades

### Para o Operador
- ✅ Validação instantânea com feedback visual e sonoro
- 📋 Histórico das últimas 20 validações
- 📊 Estatísticas em tempo real (taxa de acerto, tempo médio)
- 🔄 Auto-focus constante no campo de código
- 🌙 Modo noturno automático

### Para o Supervisor
- 📥 Exportação de logs em JSON
- 🔄 Sincronização manual de dados
- 📊 Monitoramento de performance por operador
- 💾 Backup automático no localStorage

## 🛡️ Segurança

- HTTPS obrigatório via GitHub Pages
- Dados não sensíveis (apenas códigos e CEPs)
- Login simples sem dados críticos
- Logs armazenados localmente

## 📱 Compatibilidade

### Navegadores
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

### Dispositivos
- ✅ Desktop (Windows, Mac, Linux)
- ✅ Tablet (iPad, Android)
- ✅ Mobile (iOS 14+, Android 10+)
- ✅ Scanners USB/Bluetooth

## 🔍 Solução de Problemas

### Scanner não funciona
1. Verifique se o CEP foi configurado
2. Certifique-se que o campo está com foco
3. Configure o scanner para adicionar ENTER após leitura

### Dados não atualizam
1. Limpe o cache do navegador
2. Use o botão "Sincronizar Dados"
3. Verifique se o arquivo JSON está correto

### Performance lenta
1. Verifique a conexão de internet
2. Limpe o localStorage se muito cheio
3. Use um navegador mais recente

## 📈 Métricas de Sucesso

- ⚡ Tempo médio de validação: < 100ms
- 📱 Taxa de disponibilidade: 99.9%
- 💰 Custo mensal: R$ 0,00
- 🎯 Taxa de acerto: Depende da operação

## 🤝 Contribuindo

1. Fork o projeto
2. Crie uma branch (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto é distribuído sob a licença MIT. Veja `LICENSE` para mais informações.

## 📞 Suporte

- 📧 Email: suporte@empresa.com
- 📱 WhatsApp: (00) 0000-0000
- 📋 Issues: Use a aba Issues do GitHub

---

Desenvolvido com ❤️ para otimizar operações de bipagem