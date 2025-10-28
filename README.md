# 🌐 Site do Afinador de Violino

Este diretório contém os arquivos para hospedar a política de privacidade e app-ads.txt do aplicativo.

## 📁 Arquivos

- **`index.html`** - Política de privacidade completa
- **`app-ads.txt`** - Arquivo de validação do AdMob

## 🚀 Como Publicar no GitHub Pages

### Opção 1: Usar este repositório (Mais Fácil)

1. **Ativar GitHub Pages:**
   - Vá em: Settings → Pages
   - Source: Deploy from a branch
   - Branch: `refactor` (ou sua branch principal)
   - Folder: `/docs`
   - Clique em "Save"

2. **Aguarde alguns minutos**

3. **Seu site estará em:**
   ```
   https://nunes-lucas.github.io/afinador_violino/
   ```

4. **URLs importantes:**
   - Política: `https://nunes-lucas.github.io/afinador_violino/`
   - app-ads.txt: `https://nunes-lucas.github.io/afinador_violino/app-ads.txt`

### Opção 2: Criar repositório separado

```bash
# 1. Criar novo repositório
mkdir afinador-violino-site
cd afinador-violino-site

# 2. Copiar arquivos
cp ../afinador_violino/docs/* .

# 3. Inicializar Git
git init
git branch -M main
git add .
git commit -m "Adiciona site com política e app-ads.txt"

# 4. Criar repositório no GitHub: afinador-violino-site

# 5. Push
git remote add origin https://github.com/nunes-lucas/afinador-violino-site.git
git push -u origin main

# 6. Ativar Pages no GitHub
# Settings → Pages → Source: main → Save
```

## ⚙️ Configurar app-ads.txt

### Passo 1: Obter Publisher ID

1. Acesse: https://admob.google.com
2. Clique em "Configurações" (⚙️)
3. "Informações da conta"
4. Copie o **Publisher ID** (formato: `pub-XXXXXXXXXXXXXXXX`)

### Passo 2: Editar app-ads.txt

Abra `docs/app-ads.txt` e substitua:

```
google.com, pub-XXXXXXXXXXXXXXXX, DIRECT, f08c47fec0942fa0
```

Por:

```
google.com, pub-1234567890123456, DIRECT, f08c47fec0942fa0
```
*(Use seu Publisher ID real)*

### Passo 3: Commit e Push

```bash
git add docs/app-ads.txt
git commit -m "Atualiza Publisher ID no app-ads.txt"
git push
```

## 🔗 Configurar no Google Play Console

1. Acesse: https://play.google.com/console
2. Selecione "Afinador de Violino"
3. Vá em: **Conteúdo do app → app-ads.txt**
4. Clique em: **"Adicionar arquivo app-ads.txt"**
5. Selecione: **"Hospedar no domínio do site do desenvolvedor"**
6. Digite: `nunes-lucas.github.io/afinador_violino`
7. Clique em **"Salvar"**

## ✅ Testar

### Testar Política de Privacidade
Acesse no navegador:
```
https://nunes-lucas.github.io/afinador_violino/
```

### Testar app-ads.txt
Acesse no navegador:
```
https://nunes-lucas.github.io/afinador_violino/app-ads.txt
```

Deve mostrar:
```
google.com, pub-XXXXXXXXXXXXXXXX, DIRECT, f08c47fec0942fa0
```

## ⏱️ Verificação

- **GitHub Pages deploy:** 2-5 minutos
- **AdMob verificação:** 24-48 horas
- **Status no AdMob:** Apps → Seu App → Verificar status

## 📝 Notas

- O arquivo `app-ads.txt` deve estar na raiz do domínio
- Formato deve ser exatamente como especificado
- Não adicione linhas em branco extras
- Aguarde 24-48h para verificação completa

## 🆘 Problemas?

### "Arquivo não encontrado"
- Verifique se GitHub Pages está ativo
- Aguarde 5-10 minutos após ativar
- Teste em navegador anônimo

### "Formato inválido"
- Copie exatamente o formato do exemplo
- Verifique se não há espaços extras
- Confirme que usou seu Publisher ID correto

### "Publisher ID não corresponde"
- Confirme o Publisher ID no AdMob
- Formato deve ser: `pub-` seguido de números
- Não use o Application ID (que tem `~`)

## 📚 Referências

- [GitHub Pages Docs](https://docs.github.com/pages)
- [AdMob app-ads.txt](https://support.google.com/admob/answer/9363762)
- [Documentação completa](../APP_ADS_CONFIG.md)
