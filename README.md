# Análise de notícias do Ministério da Saúde

Utilizamos o site do MInistério da Saúde: https://www.gov.br/saude/pt-br/assuntos/noticias?b_start:int=0 para coletar informações acerca das notícias do Ministério da Saúde, percebemos que em cada página continha 15 notícias com o padrão de url: https://www.gov.br/saude/pt-br/assuntos/noticias?b_start:int=p, sendo p a quantidade de notícias acumuladas, ou seja, na primeira página p = 15, na segunda página p = 30, na terceira página p = 45 e assim por diante. Vasculhamos 1653 notícias e coletamos as seguintes informações de cada uma: 

informacoes = {
        "url": full_url,
        "titulo": title,
        "descricao": description,
        "subtitulo": subtitle,
        "categoria": categoria,
        "autora": nome_autora,
        "tags": tags,
        "data_publi": data_formatada,
        "texto": texto_materia
    }

    
