![GitHub stars][github stars]
[![GitHub Workflow Status][github workflow status]][github actions link]
[![Download][download badge]][github latest release]
[![License][license badge]][github latest release]

# Теория Категорий для Программистов (Русский перевод)

**Русский перевод** книги "**C**ategory **T**heory **F**or **P**rogrammers"
от [Bartosz Milewski][bartosz github], основанной на его [серии постов в блоге][blogpost series].

Оригинальная английская версия: [hmemcpy/milewski-ctfp-pdf][original repo]

![Category Theory for Programmers][ctfp image]

## О переводе

Это полный перевод книги на русский язык, включающий:

- ✅ Все 31 главу (Часть 1, Часть 2, Часть 3)
- ✅ Предисловие и дополнительные материалы
- ✅ Обложку с оригинальным дизайном
- ✅ Все примеры кода на Haskell и C++

Перевод выполнен с сохранением терминологии теории категорий и программирования.

## Скачать книгу

Последняя версия русского перевода доступна в разделе [Releases][github latest release].

## Собрать книгу

Для сборки книги требуется [Nix][nix website]. После [установки Nix][nix download website] 
необходимо включить функцию "flake", которая должна быть [включена вручную][nixos wiki flake].

После этого выполните команду для сборки:

```bash
# Для сборки русской версии (Haskell edition)
nix build --extra-experimental-features 'nix-command flakes' .#ctfp
```

После успешной компиляции PDF файл будет помещён в директорию `result/ctfp.pdf`.

### Альтернативный способ с Makefile

Команда `nix develop` предоставит оболочку со всеми необходимыми зависимостями 
для ручной сборки книги с использованием `Makefile`:

```bash
nix develop
make ctfp
```

## Структура перевода

Русский перевод находится непосредственно в файлах глав:
- `src/content/0.0/preface.tex` - Предисловие
- `src/content/1.*/` - Часть 1 (главы 1.1-1.10)
- `src/content/2.*/` - Часть 2 (главы 2.1-2.6)
- `src/content/3.*/` - Часть 3 (главы 3.1-3.15)
- `src/half-title.tex` - Обложка и титульные страницы

## Вклад в проект

Приветствуются исправления опечаток, улучшения перевода и технические правки.
Для внесения изменений создайте pull request.

## Благодарности

- **[Bartosz Milewski][bartosz github]** - автор оригинальной книги
- **[Andres Raba][andres raba github]** - LaTeX шаблон и инструменты
- **[Igal Tabachnik (hmemcpy)][original repo]** - поддержка и развитие PDF версии

Оригинальные благодарности от Bartosz собраны на странице _Благодарности_ в конце книги.

## Лицензия

PDF книга, `.tex` файлы и связанные изображения и рисунки в директориях 
`src/fig` и `src/content` лицензированы под [Creative Commons 
Attribution-ShareAlike 4.0 International License][license cc by sa].

Скриптовые файлы лицензированы под [GNU General Public License version 3][license gnu gpl].

[download badge]:
  https://img.shields.io/badge/Download-latest-green.svg?style=flat-square
[github actions link]: https://github.com/OrelSokolov/milewski-ctfp-pdf/actions
[github stars]:
  https://img.shields.io/github/stars/OrelSokolov/milewski-ctfp-pdf.svg?style=flat-square
[github workflow status]:
  https://img.shields.io/github/actions/workflow/status/OrelSokolov/milewski-ctfp-pdf/nix-flake-check.yaml?branch=master&style=flat-square
[github latest release]:
  https://github.com/OrelSokolov/milewski-ctfp-pdf/releases/latest
[license badge]:
  https://img.shields.io/badge/License-CC_By_SA-green.svg?style=flat-square
[ctfp image]:
  https://user-images.githubusercontent.com/601206/47271389-8eea0900-d581-11e8-8e81-5b932e336336.png
[bartosz github]: https://github.com/BartoszMilewski
[nixos wiki flake]: https://wiki.nixos.org/wiki/Flakes
[andres raba github]: https://github.com/sarabander
[original repo]: https://github.com/hmemcpy/milewski-ctfp-pdf
[contributors]: https://github.com/OrelSokolov/milewski-ctfp-pdf/graphs/contributors
[license cc by sa]: https://spdx.org/licenses/CC-BY-SA-4.0.html
[license gnu gpl]: https://spdx.org/licenses/GPL-3.0.html
[blogpost series]:
  https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/
[buy regular edition on blurb]:
  https://www.blurb.com/b/9621951-category-theory-for-programmers-new-edition-hardco
[buy scala edition on blurb]:
  https://www.blurb.com/b/9603882-category-theory-for-programmers-scala-edition-pape
[v1.3.0 github release link]:
  https://github.com/hmemcpy/milewski-ctfp-pdf/releases/tag/v1.3.0
[nix website]: https://nixos.org/nix/
[nix download website]: https://nixos.org/download.html
