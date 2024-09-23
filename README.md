# Apresentação de Lucas

Este é um projeto Python que exibe uma apresentação animada sobre mim, Lucas, incluindo minha experiência profissional, habilidades técnicas e algumas informações interessantes.

## Código

```python
import time
import random

nome = "Lucas"
profissoes = ["Programador em Python", "Especialista em SQL", "Automatizador com VBA e UiPath"]
ferramentas_bi = ["Power BI", "Qlik Sense", "R"]
experiencias = [
    {"empresa": "Bradesco Seguros", "cargo": "Estagiário", "anos": 2},
    {"empresa": "CSN", "cargo": "Analista de Desempenho Jr.", "anos": 1},
    {"empresa": "CSN", "cargo": "Analista de Desempenho Pleno", "anos": 1}
]
formacao = [
    {"curso": "Nanotecnologia", "instituicao": "Universidade Federal do Rio de Janeiro"},
    {"curso": "MBA em Finanças e Gestão de Risco", "instituicao": "Universidade Federal do Rio de Janeiro"}
]

def exibir_animado(texto, delay=0.05):
    for char in texto:
        print(char, end="", flush=True)
        time.sleep(delay)
    print()

def apresentacao():
    exibir_animado(f"Olá, meu nome é {nome}!")
    exibir_animado("Aqui estão algumas coisas sobre mim:")
    
    exibir_animado("\nProfissões:")
    for profissao in profissoes:
        exibir_animado(f"- {profissao}")
    
    exibir_animado("\nFerramentas de BI que eu domino:")
    for ferramenta in ferramentas_bi:
        exibir_animado(f"- {ferramenta}")
    
    exibir_animado("\nExperiência Profissional:")
    for experiencia in experiencias:
        exibir_animado(f"- {experiencia['cargo']} na {experiencia['empresa']} ({experiencia['anos']} anos)")
    
    exibir_animado("\nFormação Acadêmica:")
    for curso in formacao:
        exibir_animado(f"- {curso['curso']} pela {curso['instituicao']}")

    exibir_animado("\nAgora algo interessante...")
    mensagens_aleatorias = [
        "Já pensou em como nanotecnologia e finanças podem estar conectadas? Eu já!",
        "Automatizar processos é como dar vida às máquinas, e eu sou o maestro disso.",
        "Finanças podem ser arriscadas, mas eu gosto de viver no limite dos dados!"
    ]
    exibir_animado(random.choice(mensagens_aleatorias))

apresentacao()
