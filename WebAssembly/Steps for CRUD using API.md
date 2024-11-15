
Make ready one asp.net core web api with CORS enabled 

create webassembly project >

Add Models, Interfaces,Services Folders

Add ICategoryService interface
```cs 
public interface ICategoryService
 {
     Task<IEnumerable<Category>> GetCategoriesAsync();
     Task<Category> GetCategoryAsync(int id);
     Task<bool> UpdateCategoryAsync(int id, Category category);
     Task<Category> CreateCategoryAsync(Category category);
     Task<bool> DeleteCategoryAsync(int id);
 }
 ```
 Add CategoryService in Services Folder
```cs
 using BlazorWeAssemblyDemo1.Interfaces;
using BlazorWeAssemblyDemo1.Models;
using System.Net.Http.Json;

namespace BlazorWeAssemblyDemo1.Services
{
    public class CategoryService:ICategoryService
    {
        private readonly HttpClient _httpClient;
        private readonly IConfiguration _configuration;

        public CategoryService(HttpClient httpClient, IConfiguration configuration)
        {
            _httpClient = httpClient;
            _configuration = configuration;
        }

        public async Task<IEnumerable<Category>> GetCategoriesAsync()
        {

            return await _httpClient.GetFromJsonAsync<IEnumerable<Category>>("api/Categories");
        }

        public async Task<Category> GetCategoryAsync(int id)
        {
            return await _httpClient.GetFromJsonAsync<Category>($"api/Categories/{id}");
        }

        public async Task<bool> UpdateCategoryAsync(int id, Category category)
        {
            var response = await _httpClient.PutAsJsonAsync($"api/Categories/{id}", category);
            return response.IsSuccessStatusCode;
        }

        public async Task<Category> CreateCategoryAsync(Category category)
        {
            var response = await _httpClient.PostAsJsonAsync("api/Categories", category);
            if (response.IsSuccessStatusCode)
            {
                return await response.Content.ReadFromJsonAsync<Category>();
            }

            return null;
        }

        public async Task<bool> DeleteCategoryAsync(int id)
        {
            var response = await _httpClient.DeleteAsync($"api/Categories/{id}");
            return response.IsSuccessStatusCode;
        }
    }
}
```

In Pages folder ==> Categories.razor Component
```razor


```