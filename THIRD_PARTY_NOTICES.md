# Bibliotecas de terceiros — MMARTINS BOOST v1.1.0

O MMARTINS BOOST contém código próprio e bibliotecas de terceiros. A licença do aplicativo não substitui nem restringe os direitos concedidos pelas licenças dessas bibliotecas.

## Qt / PySide6

- Versão da interface Qt for Python / PySide6: **6.12.0**.
- Componentes Qt WebEngine / Qt PDF identificados na compilação: **6.12.0.140** (distribuições Python).
- Os componentes Qt podem estar disponíveis sob **LGPLv3**, **GPLv3** ou outras condições, conforme o módulo e componentes incorporados. A distribuição de um aplicativo proprietário exige que as condições das bibliotecas LGPL efetivamente utilizadas sejam cumpridas, incluindo fornecimento/oferta adequada das fontes correspondentes, avisos, cópias das licenças e a possibilidade de substituir e executar bibliotecas modificadas nos termos da licença.
- **Qt WebEngine** incorpora componentes Chromium sujeitos a outras licenças e avisos próprios. Esses avisos também precisam acompanhar a distribuição quando aplicáveis.

Fontes oficiais:
- https://doc.qt.io/qt-6/licensing.html
- https://www.qt.io/development/open-source-lgpl-obligations
- https://doc.qt.io/qt-6/licenses-used-in-qt.html
- https://doc.qt.io/qt-6/qtwebengine-licensing.html

## FFmpeg

- A distribuição Windows v1.1.0 inclui, conforme inventário do instalador testado, **`ffmpeg-win-x86_64-v9.0.2.exe`** pela dependência `imageio-ffmpeg==0.8.1`.
- Esse executável reporta `ffmpeg version 9.0.2-essentials_build-www.gyan.dev`, compilado com `--enable-gpl --enable-version3`; sua saída de `ffmpeg -L` declara **GNU GPL, versão 3 ou posterior**.
- É necessário disponibilizar o **código-fonte correspondente à compilação específica**, incluindo informações sobre bibliotecas externas, alterações e instruções de compilação conforme as obrigações aplicáveis. Uma indicação genérica do repositório FFmpeg não substitui necessariamente esses materiais.
- A licença do wrapper Python `imageio-ffmpeg` é distinta da licença do executável FFmpeg incluído.

Fontes oficiais:
- https://ffmpeg.org/legal.html
- https://www.gyan.dev/ffmpeg/builds/
- https://github.com/imageio/imageio-ffmpeg

## Outras dependências identificadas

- `psutil==7.2.2` — licença BSD-3-Clause.
- `Send2Trash==1.8.3` — licença BSD-3-Clause.
- `websocket-client==1.9.2` — licença Apache-2.0.
- `certifi==2026.10.23` — conferir os avisos da distribuição efetivamente empacotada.
- `PyInstaller==6.22.3` — ferramenta de empacotamento; conferir condições da exceção de licença aplicável ao bootloader incluído.

A pasta `LICENCAS` do instalador deve conter os textos integrais e avisos correspondentes aos componentes efetivamente distribuídos, além dos materiais de código-fonte ou da oferta e instruções exigidas pelas licenças aplicáveis.

## Pendências de distribuição (não são declaração de cumprimento)

Este documento identifica componentes, mas **não certifica conformidade jurídica**. Antes de publicar o instalador, é necessário concluir e conferir:

1. Disponibilização ou oferta válida, sob responsabilidade do distribuidor, dos códigos-fonte correspondentes e instruções aplicáveis ao Qt LGPL, componentes Qt WebEngine e FFmpeg GPLv3.
2. Licenças e avisos completos dos componentes nativos/Chromium realmente incluídos no instalador, não apenas dos pacotes Python.
3. Mecanismo e instruções para substituição/religação das bibliotecas Qt nos termos da LGPL.
4. Coerência entre os arquivos efetivamente instalados, os metadados das versões e os materiais de licença distribuídos.

**Observação:** a versão 9.0.2 substitui a menção à versão 7.1 encontrada em uma documentação anterior do projeto. Isso não altera o número de versão do MMARTINS BOOST (v1.1.0).
