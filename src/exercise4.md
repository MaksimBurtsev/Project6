# Задание №4. Эндпоинты

| Описание | {METHOD} | api/{VERSION} | {CLASS} | URL |
| --- | --- | --- | --- | --- |
| Получение списка рецептов в конкретной категории | GET | /api/v1/categories/{category_id}/recipes | Recipes | https://new-year-kitchen.com/api/v1/categories/1/recipes |
| Добавление ингредиента в определенный рецепт | POST | /api/v1/recipes/{recipe_id}/ingredients | Ingredients | https://new-year-kitchen.com/api/v1/recipes/1/ingredients |
| Изменение порядка следования рецептов в категории | PUT | /api/v1/categories/{category_id}/recipes/reorder | Recipes | https://new-year-kitchen.com/api/v1/categories/1/recipes/reorder |
| Удаление рецепта | DELETE | /api/v1/recipes/{recipe_id} | Recipes | https://new-year-kitchen.com/api/v1/recipes/1 |