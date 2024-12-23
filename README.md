# Análise de Notícias do Ministério da Saúde

Utilizamos o site do MInistério da Saúde: https://www.gov.br/saude/pt-br/assuntos/noticias?b_start:int=0 para coletar informações acerca das notícias do Ministério da Saúde, percebemos que em cada página continha 15 notícias com o padrão de url: https://www.gov.br/saude/pt-br/assuntos/noticias?b_start:int=p, sendo p a quantidade de notícias acumuladas, ou seja, na primeira página p = 15, na segunda página p = 30, na terceira página p = 45 e assim por diante. Vasculhamos 1653 notícias e coletamos as seguintes informações de cada uma: 

informacoes = { \\
        "url": full_url,\\
        "titulo": title,
        "descricao": description,
        "subtitulo": subtitle,
        "categoria": categoria,
        "autora": nome_autora,
        "tags": tags,
        "data_publi": data_formatada,
        "texto": texto_materia
    }

Após coletar o dados, fizemos uma análise descritiva:

1. Frequência de notícias por período (março-2024 a dezembro 2024)
2. Top 20 Tags mais utilizadas nas notícias entre esse período
3. Analisamos a Similiridade Textual entre os subtítulos das notícias, com objetivo de encontrar as manchetes com subtítulos parecidos para isto usando a biblioteca TfidfVectorizer do Python que é usada para converter uma coleção de documentos de texto em uma matriz de características. Basicamente, TF-IDF é uma técnica que reflete a importância de uma palavra em um documento em relação a uma coleção de documentos (corpus). Ela é composta por duas partes:

-> *TF (Term Frequency)*: Mede a frequência de uma palavra em um documento.
-> *IDF (Inverse Document Frequency)*: Mede a importância de uma palavra em todo o corpus. Palavras comuns em muitos documentos têm um valor IDF baixo.

4. Depois usamos a vetorização TF-IDF para calcular a similaridade entre os subtítulos com base nas tags. 
