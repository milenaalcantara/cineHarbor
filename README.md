# Today Movies 🎬

Este projeto foi criado com UIKit + ViewCode para servir como base de aprendizado para desenvolvedores que já conhecem Swift e SwiftUI. O foco é entender como construir uma aplicação totalmente programática com UIKit, fazendo consumo de API e persistência com CoreData.

---

## ✅ Funcionalidades Implementadas

* [x] Listagem infinita de filmes populares do dia (scroll infinito)
* [x] Tela de detalhes com descrição, imagem e data de lançamento
* [x] Favoritar filme com persistência via CoreData
* [x] Tela de favoritos

---

## 🧩 Tecnologias Utilizadas

* UIKit
* ViewCode (sem Storyboards ou XIBs)
* URLSession + Codable para consumo da API do TMDB
* CoreData
* AutoLayout programático com NSLayoutConstraint ou NSLayoutAnchor

---

## 📂 Estrutura do Projeto

```
MoviesApp/
├── Modules/
│   ├── MoviesList/         # Tela com lista infinita de filmes
│   ├── MovieDetails/       # Tela de detalhes do filme
│   └── Favorites/          # Tela com filmes salvos no CoreData
│
├── Network/               # Camada de serviço para consumir a API
│   └── TMDBService.swift
│
├── Persistence/           # CoreData Stack e helpers
│
├── Extensions/            # Extensões úteis
│
├── Resources/             # Imagens, Assets, Fonts, etc
│
├── AppDelegate.swift
├── SceneDelegate.swift
└── README.md
```

Cada pasta de módulo (ex: `MoviesList`) contém:

* `ViewController.swift`
* `ViewModel.swift` (opcional para organização)
* `README.md` explicando o fluxo

---

## 💡 Como rodar o projeto

1. Clone o repositório

```bash
git clone https://github.com/milenaalcantara/cineHarbor.git
```

2. Abra o `.xcworkspace` no Xcode

3. Insira sua chave da API do TMDB no arquivo `Secrets.swift`

```swift
struct Secrets {
    static let apiKey = "SUA_API_KEY_AQUI"
}
```

4. Rode o app em um simulador ou dispositivo

---

## 🎓 Desafios sugeridos para o aluno

1. [ ] Adicionar listagem de séries do dia (`trending/tv/day`)
2. [ ] Criar uma tela combinando filmes + séries
3. [ ] Adicionar busca por título (filmes e/ou séries)
4. [ ] Implementar modo offline para favoritos
5. [ ] Mostrar último filme/série visto ao abrir o app
6. [ ] Adicionar testes de unidade para camada de rede

---

## 🚀 API Utilizada: TMDB

* Base URL: `https://api.themoviedb.org/3`
* Endpoints usados:

  * `/trending/movie/day`
  * `/movie/{movie_id}`

Documentação oficial: [https://developer.themoviedb.org/](https://developer.themoviedb.org/)

---

## 😊 Licença

Este projeto é de uso educacional e pode ser reutilizado para fins de aprendizado.

---

> Feito com ❤️ para ensinar UIKit na prática.
