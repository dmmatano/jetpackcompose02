# Jetpack Compose 02 - With Full Review

### Layouts padrão
Existem 3 elementos de layout padrão no compose: 
- Column: um embaixo do outro
- Row: em fila
- Box: um "emcima" do outro (eixo z)
<br>

### State e MutableState
State e MutableState são interfaces que possuem um valor e "aciona" a atualização UI (recomposição)<br>
Ao adicionar variaveis dentro de um @Composable, ela pode ser "resetada" devido as atualizações<br>
frequentes do UI. Use remember{ } para lembrar do estado da variável mesmo após as recomposições.<br>

### LazyColumn e LazyRow
São equivalentes ao RecyclerView. Ao invés de "reciclar" as view, o LazyColumn/LazyRow cria novos composables.

### rememberSaveable
Se rotacionarmos a tela ou o processo morrer, o remember é resetado, pois a activity morre nessa troca 
de configuração. Use rememberSaveable para manter mesmo em mudanças de configurações. 

### Animations
De high level API a low level. Veja a documentação: <br>
https://developer.android.com/develop/ui/compose/animation/introduction?hl=pt-br <br>
Qualquer animação animate*AsState pode ser interrompida, ou seja, se o targetValue mudar durante a animação, <br>
ela reinicia a partir do novo targetValue

### Estilo
Presente em ui.theme.Theme.kt<br>
MaterialTheme tem as propriedades colorScheme, typography e shapes<br>
Podemos usar .copy para alterar um estilo, mas busque utilizar o recomendado pelo Google/Android.
