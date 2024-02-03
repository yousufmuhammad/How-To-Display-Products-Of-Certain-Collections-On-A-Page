If this page has the .liquid extension, then you can display the products by adding the following code:

{% for product in collections.all.products %}
  {% for collection in product.collections %}
    {% if collection.title == 'CERTAIN_COLLECTION_TITLE' %} 

Here you need to replace the name of the collection that you would like to display.

  
      <div class="product-item">
        <img src="{{ product.featured_image | product_img_url: 'medium' }}" alt="{{ product.title | escape  }}" />    
        <a class="shop-now" href="{{ product.url }}">{{ product.title | escape  }}</a>      
      </div>
    {% endif %}
  {% endfor %}
{% endfor %}





P.S We added HTML tags for an example, but you can write them in the form that is necessary for you.
