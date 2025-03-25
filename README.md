# Processador de Imagens Python

Um pacote Python robusto e flexível para processamento de imagens, implementando conceitos de programação orientada a objetos e boas práticas de desenvolvimento.

## Funcionalidades

- Leitura e salvamento de imagens em diversos formatos (JPEG, PNG, BMP)
- Transformações básicas (redimensionamento, rotação, recorte, espelhamento)
- Filtros e efeitos (blur, sharpen, grayscale)
- Manipulação de canais de cor (RGB, CMYK)
- Interface de linha de comando (CLI)

## Instalação

```bash
pip install -e .
```

## Uso

### Via Interface de Linha de Comando

```bash
python -m image_processor.cli --input imagem.jpg --output imagem_processada.jpg --resize 800x600 --rotate 90
```

### Via API Python

```python
from image_processor import ImageProcessor

# Carregar uma imagem
processor = ImageProcessor("imagem.jpg")

# Aplicar transformações
processor.resize(800, 600)
processor.rotate(90)
processor.apply_filter("blur")

# Salvar a imagem processada
processor.save("imagem_processada.jpg")
```

## Estrutura do Projeto

```
image_processor/
├── __init__.py
├── core/
│   ├── __init__.py
│   ├── image.py
│   └── transformations.py
├── filters/
│   ├── __init__.py
│   └── effects.py
├── utils/
│   ├── __init__.py
│   └── helpers.py
└── cli.py
```

## Requisitos

- Python 3.8+
- Pillow (PIL)
- OpenCV (opcional)

## Desenvolvimento

Para contribuir com o projeto:

1. Clone o repositório
2. Instale as dependências de desenvolvimento: `pip install -e ".[dev]"`
3. Execute os testes: `pytest`

## Licença

MIT 