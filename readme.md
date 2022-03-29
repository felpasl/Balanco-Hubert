# Extração de dados do portal do condomino Hubert:

Criar um arquivo .env com as credenciais de acesso e Data de inicio da extração:

```
USER=usuario
PASS=senha
FROM=2020-04
```
O diretório está preparado para usar o [VSCode Remote com docker](https://code.visualstudio.com/docs/remote/containers), 

O código em python está em um jupter notebook `importBalanco.ipynb` 

as execuções de cada code block seguem em ordem com comentários

1. Os arquivos sao baixados utilizando [Selenium em python](https://selenium-python.readthedocs.io/)
2. O html é armazenado no diretorio `contashtml/` 
3. O html é lido utilizando [Beautifulsoap4](https://beautiful-soup-4.readthedocs.io/en/latest/)
4. Os [Dataframes](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html) extraídos são formatados renomeados e armazenados no excel de saída `output.xlsx`

A partir deste arquivo `output.xlsx` os dados podem ser lidos e formatados servindo de fonte para gráficos e análises.