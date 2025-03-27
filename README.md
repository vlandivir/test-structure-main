# Test of git structure

## test-structure-main

```bash
# Добавляем удаленный репозиторий с именем 'sub-repo'
git remote add -f test-structure-external https://github.com/vlandivir/test-structure-external.git

# Добавляем subtree в папку 'external'
git subtree add --prefix=external test-structure-external main --squash

# Получаем обновления
git subtree pull --prefix=external test-structure-external main --squash -m"Auto merge"

# Отправляем изменения
git subtree push --prefix=external test-structure-external main
