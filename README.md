****# Laravel sunday streaming

## Stream 1 - seeding

php artisan db:seed --class=PostSeeder

### Seeding with a factory


```
class PostFactory extends Factory
{
    protected $model = Post::class;
    /**
    * Define the model's default state.
    *
    * @return array<string, mixed>
    */
    public function definition(): array
    {
        return [
            'title' => implode(' ', fake()->words),
            'author' => fake()->firstName . ' ' . fake()->lastName,
            'content' => fake()->realText,
        ];
    }
}
```
