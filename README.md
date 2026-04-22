# festival

Em urls.py:

Adicionei a rota para a página dos dias (path('dias/', views.dias_view, name='dias')), que estava em falta e impedia o menu de funcionar.

Em views.py:

Importei os modelos Dia e Concerto no topo do ficheiro (antes só estava o Palco).
Criei a função palcos_view que estava em falta.
Completei a concerto_view que estava inacabada, para ir buscar o concerto pelo ID (Concerto.objects.get(id=id)).

Nos ficheiros .html:

dias.html: Criei este ficheiro de raiz. Fiz um ciclo for para mostrar os dias e, lá dentro, usei a relação inversa dia.concertos.all para listar as bandas de cada dia.
palcos.html: Os links para os detalhes do concerto estavam vazios (href=""). Corrigi usando a tag {% url 'concerto' concerto.id %} para criar os links automáticos.
