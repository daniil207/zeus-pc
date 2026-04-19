# Zeus PC

Статический сайт для GitHub Pages.

## Как опубликовать на GitHub Pages

1. Создать новый публичный репозиторий на GitHub, например `zeus-pc`.
2. Загрузить в корень репозитория файлы:
   - `index.html`
   - `CNAME`
   - `.nojekyll`
   - `README.md`
3. Открыть `Settings` -> `Pages`.
4. В блоке `Build and deployment` выбрать:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
5. Нажать `Save`.
6. В поле `Custom domain` указать `zeus-pk.ru`, если GitHub не подхватил домен из файла `CNAME`.
7. После проверки домена включить `Enforce HTTPS`.

## DNS для домена

У регистратора домена нужно убрать записи Tilda и добавить записи для GitHub Pages.

Для корневого домена `zeus-pk.ru` нужны A-записи:

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Для `www.zeus-pk.ru` нужна CNAME-запись:

```text
www -> <github-username>.github.io
```

`<github-username>` нужно заменить на имя аккаунта GitHub.

DNS может обновляться от нескольких минут до 24 часов.
