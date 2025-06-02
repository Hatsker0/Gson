item_cart.xml

<?xml version="1.0" encoding="utf-8"?>
<androidx.cardview.widget.CardView xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_margin="8dp"
    app:cardCornerRadius="8dp"
    app:cardElevation="4dp">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:padding="16dp">

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">

            <ImageView
                android:id="@+id/product_image"
                android:layout_width="80dp"
                android:layout_height="80dp"
                android:contentDescription="Product image"
                android:scaleType="centerCrop" />

            <LinearLayout
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:orientation="vertical"
                android:paddingStart="16dp">

                <TextView
                    android:id="@+id/product_name"
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    android:textSize="18sp"
                    android:textStyle="bold" />

                <TextView
                    android:id="@+id/product_price"
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    android:textColor="@android:color/holo_green_dark"
                    android:textSize="16sp" />
            </LinearLayout>
        </LinearLayout>

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:gravity="end"
            android:orientation="horizontal"
            android:paddingTop="8dp">

            <Button
                android:id="@+id/btn_details"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="О товаре"
                android:textSize="14sp" />

            <Button
                android:id="@+id/btn_add_to_cart"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_marginStart="8dp"
                android:text="Удалить"
                android:textSize="14sp" />
        </LinearLayout>
    </LinearLayout>
</androidx.cardview.widget.CardView>

item_product.xml

<?xml version="1.0" encoding="utf-8"?>
<androidx.cardview.widget.CardView xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_margin="8dp"
    app:cardCornerRadius="8dp"
    app:cardElevation="4dp">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:padding="16dp">

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">

            <ImageView
                android:id="@+id/product_image"
                android:layout_width="80dp"
                android:layout_height="80dp"
                android:contentDescription="Product image"
                android:scaleType="centerCrop" />

            <LinearLayout
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:orientation="vertical"
                android:paddingStart="16dp">

                <TextView
                    android:id="@+id/product_name"
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    android:textSize="18sp"
                    android:textStyle="bold" />

                <TextView
                    android:id="@+id/product_price"
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    android:textColor="@android:color/holo_green_dark"
                    android:textSize="16sp" />
            </LinearLayout>
        </LinearLayout>

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:gravity="end"
            android:orientation="horizontal"
            android:paddingTop="8dp">

            <Button
                android:id="@+id/btn_details"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="О товаре"
                android:textSize="14sp" />

            <Button
                android:id="@+id/btn_add_to_cart"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_marginStart="8dp"
                android:text="В корзину"
                android:textSize="14sp" />
        </LinearLayout>
    </LinearLayout>
</androidx.cardview.widget.CardView>

fragment_gallery.xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.coordinatorlayout.widget.CoordinatorLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:fitsSystemWindows="true"
    tools:context=".ui.gallery.GalleryFragment">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="vertical">

        <androidx.appcompat.widget.SearchView
            android:id="@+id/search_view_products"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginStart="8dp"
            android:layout_marginEnd="8dp"
            android:layout_marginTop="?attr/actionBarSize"
        android:layout_marginBottom="8dp"
        android:iconifiedByDefault="false"
        android:queryHint="Поиск по товарам" />

        <androidx.recyclerview.widget.RecyclerView
            android:id="@+id/recycler_view_products"
            android:layout_width="match_parent"
            android:layout_height="0dp"
            android:layout_weight="1"
            android:clipToPadding="false"
            android:paddingBottom="8dp" />

    </LinearLayout>

</androidx.coordinatorlayout.widget.CoordinatorLayout>

fragment_home.xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:fitsSystemWindows="true"
    tools:context=".ui.home.HomeFragment">

    <TextView
        android:id="@+id/tv_empty_cart"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:gravity="center"
        android:text="Корзина пуста"
        android:textSize="18sp"
        android:visibility="gone" />

    <androidx.recyclerview.widget.RecyclerView
        android:id="@+id/recycler_view_cart"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:paddingTop="?attr/actionBarSize" />

    <TextView
        android:id="@+id/tv_total_price"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:padding="16dp"
        android:textAlignment="center"
        android:textSize="18sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/btn_clear_cart"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="16dp"
        android:text="Очистить корзину" />
</LinearLayout>

ProductDetailActivity.java

package com.example.demo;

import android.os.Bundle;
import android.widget.Button;
import android.widget.ImageView;
import android.widget.TextView;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

import com.example.demo.models.Cart;
import com.example.demo.models.Product;

public class ProductDetailActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_product_detail);

        // Получаем переданный товар
        Product product = (Product) getIntent().getSerializableExtra("product");

        if (product != null) {
            // Находим элементы интерфейса
            ImageView productImage = findViewById(R.id.product_detail_image);
            TextView productName = findViewById(R.id.product_detail_name);
            TextView productPrice = findViewById(R.id.product_detail_price);
            TextView productDescription = findViewById(R.id.product_detail_description);
            Button addToCartBtn = findViewById(R.id.btn_add_to_cart);

            // Заполняем данными
            productImage.setImageResource(product.getImageResId());
            productName.setText(product.getName());
            productPrice.setText(String.format("%.2f ₽", product.getPrice()));
            productDescription.setText(product.getDescription());

            addToCartBtn.setOnClickListener(v -> {
                Cart.getInstance().addProduct(product, ProductDetailActivity.this);
                Toast.makeText(ProductDetailActivity.this,
                        product.getName() + " добавлен в корзину",
                        Toast.LENGTH_SHORT).show();
            });
        }
    }
}

GalleryFragment.java
package com.example.demo.ui.gallery;

import android.content.Intent;
import android.os.Bundle;
import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.Toast;

import androidx.annotation.NonNull;
import androidx.appcompat.widget.SearchView; // <-- добавлен импорт
import androidx.fragment.app.Fragment;
import androidx.recyclerview.widget.LinearLayoutManager;
import androidx.recyclerview.widget.RecyclerView;

import com.example.demo.ProductDetailActivity;
import com.example.demo.R;
import com.example.demo.adapters.ProductAdapter;
import com.example.demo.models.Cart;
import com.example.demo.models.Product;

import java.util.ArrayList;
import java.util.List;

public class GalleryFragment extends Fragment implements ProductAdapter.OnProductClickListener {

    private List<Product> fullProductList;
    private ProductAdapter adapter;

    @Override
    public View onCreateView(@NonNull LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState) {
        View root = inflater.inflate(R.layout.fragment_gallery, container, false);

        RecyclerView recyclerView = root.findViewById(R.id.recycler_view_products);
        recyclerView.setLayoutManager(new LinearLayoutManager(getContext()));

        SearchView searchView = root.findViewById(R.id.search_view_products); // <-- SearchView должен быть в fragment_gallery.xml

        fullProductList = initializeProducts();

        adapter = new ProductAdapter(new ArrayList<>(fullProductList), this, requireContext());
        recyclerView.setAdapter(adapter);

        // Обработка текста поиска
        searchView.setOnQueryTextListener(new SearchView.OnQueryTextListener() {
            @Override
            public boolean onQueryTextSubmit(String query) {
                filterProducts(query);
                return true;
            }

            @Override
            public boolean onQueryTextChange(String newText) {
                filterProducts(newText);
                return true;
            }
        });

        return root;
    }

    private void filterProducts(String query) {
        List<Product> filteredList = new ArrayList<>();
        String lowerCaseQuery = query.toLowerCase();

        for (Product product : fullProductList) {
            if (product.getName().toLowerCase().contains(lowerCaseQuery) ||
                    product.getDescription().toLowerCase().contains(lowerCaseQuery)) {
                filteredList.add(product);
            }
        }

        adapter.updateList(filteredList);
    }

    private List<Product> initializeProducts() {
        List<Product> products = new ArrayList<>();
        products.add(new Product("1", "Фильтр масляный", 500.00,
                "Бюджетный масляный фильтр, аналог оригиналу", android.R.drawable.ic_menu_info_details));
        products.add(new Product("2", "Свечи зажигания", 800.00,
                "Комплект из 4-х свечей для бензиновых двигателей", android.R.drawable.ic_menu_edit));
        products.add(new Product("3", "Тормозные колодки", 1500.00,
                "Передние тормозные колодки с хорошим ресурсом", android.R.drawable.ic_menu_compass));
        products.add(new Product("4", "Воздушный фильтр", 700.00,
                "Фильтр для двигателя, альтернатива оригиналу", android.R.drawable.ic_menu_upload));
        products.add(new Product("5", "Аккумулятор 55 Ач", 3500.00,
                "Автомобильный аккумулятор средней мощности", android.R.drawable.ic_menu_manage));
        return products;
    }

    @Override
    public void onAddToCartClick(Product product) {
        Cart.getInstance().addProduct(product, requireContext());
        Toast.makeText(getContext(),
                product.getName() + " добавлен в корзину",
                Toast.LENGTH_SHORT).show();
    }

    @Override
    public void onDetailsClick(Product product) {
        Intent intent = new Intent(getActivity(), ProductDetailActivity.class);
        intent.putExtra("product", product);
        startActivity(intent);
    }
}

HomeFragment.java

package com.example.demo.ui.home;

import android.content.Context;
import android.content.SharedPreferences;
import android.os.Bundle;
import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.Button;
import android.widget.TextView;
import android.widget.Toast;

import androidx.annotation.NonNull;
import androidx.fragment.app.Fragment;
import androidx.recyclerview.widget.LinearLayoutManager;
import androidx.recyclerview.widget.RecyclerView;

import com.example.demo.R;
import com.example.demo.adapters.CartAdapter;
import com.example.demo.models.Cart;
import com.example.demo.models.Product;

import java.io.BufferedReader;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.List;
import java.util.Locale;

public class HomeFragment extends Fragment implements CartAdapter.OnRemoveItemClickListener {

    private RecyclerView recyclerView;
    private TextView tvEmptyCart, tvTotalPrice;
    private Button btnClearCart;

    @Override
    public View onCreateView(@NonNull LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState) {
        View root = inflater.inflate(R.layout.fragment_home, container, false);

        recyclerView = root.findViewById(R.id.recycler_view_cart);
        tvEmptyCart = root.findViewById(R.id.tv_empty_cart);
        tvTotalPrice = root.findViewById(R.id.tv_total_price);
        btnClearCart = root.findViewById(R.id.btn_clear_cart);

        recyclerView.setLayoutManager(new LinearLayoutManager(getContext()));
        updateCartUI();

        btnClearCart.setOnClickListener(v -> {
            Cart.getInstance().clearCart(requireContext());
            updateCartUI();
            Toast.makeText(getContext(), "Корзина очищена", Toast.LENGTH_SHORT).show();
        });

        return root;
    }

    @Override
    public void onResume() {
        super.onResume();
        loadCartForCurrentUser();
        updateCartUI();
    }

    private void loadCartForCurrentUser() {
        SharedPreferences prefs = requireContext().getSharedPreferences("UserPrefs", Context.MODE_PRIVATE);
        String currentLogin = prefs.getString("current_login", null);

        if (currentLogin != null) {
            String userCode = getUserCode(currentLogin);
            if (userCode != null) {
                Cart.getInstance().loadUserCart(requireContext(), userCode);
            }
        }
    }

    private String getUserCode(String login) {
        try (FileInputStream fis = requireContext().openFileInput("user.txt");
             BufferedReader reader = new BufferedReader(new InputStreamReader(fis))) {

            String line;
            while ((line = reader.readLine()) != null) {
                String storedLogin = reader.readLine();
                reader.readLine(); // Пропускаем пароль
                String storedCode = reader.readLine();

                if (storedLogin != null && storedLogin.equals(login)) {
                    return storedCode;
                }
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
        return null;
    }

    private void updateCartUI() {
        List<Product> cartItems = Cart.getInstance().getProducts();
        boolean isEmpty = cartItems.isEmpty();

        recyclerView.setVisibility(isEmpty ? View.GONE : View.VISIBLE);
        tvEmptyCart.setVisibility(isEmpty ? View.VISIBLE : View.GONE);
        tvTotalPrice.setVisibility(isEmpty ? View.GONE : View.VISIBLE);
        btnClearCart.setVisibility(isEmpty ? View.GONE : View.VISIBLE);

        if (!isEmpty) {
            recyclerView.setAdapter(new CartAdapter(cartItems, this));
            double total = Cart.getInstance().getTotalPrice();
            tvTotalPrice.setText(String.format(Locale.getDefault(), "Итого: %.2f ₽", total));
        }
    }

    @Override
    public void onRemoveItemClick(Product product) {
        Cart.getInstance().removeProduct(product, requireContext());
        updateCartUI();
        Toast.makeText(getContext(),
                product.getName() + " удален из корзины",
                Toast.LENGTH_SHORT).show();
    }
}

CartAdapter.java

package com.example.demo.adapters;

import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.ImageView;
import android.widget.TextView;
import android.widget.Button;

import androidx.annotation.NonNull;
import androidx.recyclerview.widget.RecyclerView;

import com.example.demo.R;
import com.example.demo.models.Product;

import java.util.List;

public class CartAdapter extends RecyclerView.Adapter<CartAdapter.CartViewHolder> {
    private final List<Product> cartItems;
    private final OnRemoveItemClickListener removeItemClickListener;

    public interface OnRemoveItemClickListener {
        void onRemoveItemClick(Product product);
    }

    public CartAdapter(List<Product> cartItems, OnRemoveItemClickListener listener) {
        this.cartItems = cartItems;
        this.removeItemClickListener = listener;
    }

    @NonNull
    @Override
    public CartViewHolder onCreateViewHolder(@NonNull ViewGroup parent, int viewType) {
        View view = LayoutInflater.from(parent.getContext())
                .inflate(R.layout.item_cart, parent, false);
        return new CartViewHolder(view);
    }

    @Override
    public void onBindViewHolder(@NonNull CartViewHolder holder, int position) {
        Product product = cartItems.get(position);
        holder.productName.setText(product.getName());
        holder.productPrice.setText(String.format("%.2f ₽", product.getPrice()));
        holder.productImage.setImageResource(product.getImageResId());

        holder.btnRemove.setOnClickListener(v -> {
            if (removeItemClickListener != null) {
                removeItemClickListener.onRemoveItemClick(product);
            }
        });
    }

    @Override
    public int getItemCount() {
        return cartItems.size();
    }

    static class CartViewHolder extends RecyclerView.ViewHolder {
        ImageView productImage;
        TextView productName, productPrice;
        Button btnRemove;

        public CartViewHolder(@NonNull View itemView) {
            super(itemView);
            productImage = itemView.findViewById(R.id.product_image);
            productName = itemView.findViewById(R.id.product_name);
            productPrice = itemView.findViewById(R.id.product_price);
            btnRemove = itemView.findViewById(R.id.btn_add_to_cart); // Используем ту же кнопку, но меняем текст
        }
    }
}

ProductAdapter.java

package com.example.demo.adapters;

import android.content.Context;
import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.Button;
import android.widget.ImageView;
import android.widget.TextView;

import androidx.annotation.NonNull;
import androidx.recyclerview.widget.RecyclerView;

import com.example.demo.R;
import com.example.demo.models.Product;

import java.util.List;

public class ProductAdapter extends RecyclerView.Adapter<ProductAdapter.ProductViewHolder> {

    private List<Product> productList;
    private final OnProductClickListener listener;
    private final Context context;

    // Интерфейс для обработки кликов
    public interface OnProductClickListener {
        void onAddToCartClick(Product product);
        void onDetailsClick(Product product);
    }

    public ProductAdapter(List<Product> productList, OnProductClickListener listener, Context context) {
        this.productList = productList;
        this.listener = listener;
        this.context = context;
    }

    @NonNull
    @Override
    public ProductViewHolder onCreateViewHolder(@NonNull ViewGroup parent, int viewType) {
        View view = LayoutInflater.from(parent.getContext())
                .inflate(R.layout.item_product, parent, false);
        return new ProductViewHolder(view);
    }

    @Override
    public void onBindViewHolder(@NonNull ProductViewHolder holder, int position) {
        Product product = productList.get(position);
        holder.productImage.setImageResource(product.getImageResId());
        holder.productName.setText(product.getName());
        holder.productPrice.setText(String.format("%.2f ₽", product.getPrice()));

        holder.btnAddToCart.setOnClickListener(v -> listener.onAddToCartClick(product));
        holder.btnDetails.setOnClickListener(v -> listener.onDetailsClick(product));
    }

    @Override
    public int getItemCount() {
        return productList.size();
    }

    // Метод для обновления списка после фильтрации
    public void updateList(List<Product> filteredList) {
        this.productList = filteredList;
        notifyDataSetChanged();
    }

    static class ProductViewHolder extends RecyclerView.ViewHolder {
        ImageView productImage;
        TextView productName, productPrice;
        Button btnDetails, btnAddToCart;

        public ProductViewHolder(@NonNull View itemView) {
            super(itemView);
            productImage = itemView.findViewById(R.id.product_image);
            productName = itemView.findViewById(R.id.product_name);
            productPrice = itemView.findViewById(R.id.product_price);
            btnDetails = itemView.findViewById(R.id.btn_details);
            btnAddToCart = itemView.findViewById(R.id.btn_add_to_cart);
        }
    }
}

ProductDetailsDialog.java

package com.example.demo.dialogs;  // Исправлен package

import android.app.Dialog;
import android.os.Bundle;
import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.ImageView;
import android.widget.TextView;
import androidx.annotation.NonNull;
import androidx.annotation.Nullable;
import androidx.fragment.app.DialogFragment;
import com.example.demo.R;
import com.example.demo.models.Product;
import java.io.Serializable;
import java.util.Locale;

public class ProductDetailsDialog extends DialogFragment {
    private static final String ARG_PRODUCT = "product";
    private Product product;

    public static ProductDetailsDialog newInstance(Product product) {
        ProductDetailsDialog dialog = new ProductDetailsDialog();
        Bundle args = new Bundle();
        args.putSerializable(ARG_PRODUCT, (Serializable) product);  // Явное приведение к Serializable
        dialog.setArguments(args);
        return dialog;
    }

    @Override
    public void onCreate(@Nullable Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        if (getArguments() != null) {
            product = (Product) getArguments().getSerializable(ARG_PRODUCT);
        }
    }

    @NonNull
    @Override
    public Dialog onCreateDialog(@Nullable Bundle savedInstanceState) {
        Dialog dialog = super.onCreateDialog(savedInstanceState);
        dialog.setTitle("Детали товара");
        return dialog;
    }

    @Nullable
    @Override
    public View onCreateView(@NonNull LayoutInflater inflater, @Nullable ViewGroup container,
                             @Nullable Bundle savedInstanceState) {
        View view = inflater.inflate(R.layout.dialog_product_details, container, false);

        ImageView image = view.findViewById(R.id.product_image);
        TextView name = view.findViewById(R.id.product_name);
        TextView price = view.findViewById(R.id.product_price);
        TextView description = view.findViewById(R.id.product_description);

        if (product != null) {
            image.setImageResource(product.getImageResId());
            name.setText(product.getName());
            price.setText(String.format(Locale.getDefault(), "%.2f ₽", product.getPrice()));  // Добавлен Locale
            description.setText(product.getDescription());
        }

        return view;
    }
}

Cart.java

package com.example.demo.models;

import android.content.Context;
import android.content.SharedPreferences;
import android.util.Log;

import com.google.gson.Gson;
import com.google.gson.reflect.TypeToken;

import java.lang.reflect.Type;
import java.util.ArrayList;
import java.util.List;

public class Cart {
    private static final String TAG = "Cart";
    private static final String PREFS_NAME = "CartPrefs";

    private static Cart instance;
    private List<Product> products;
    private String currentUserCode;

    private Cart() {
        products = new ArrayList<>();
    }

    public static synchronized Cart getInstance() {
        if (instance == null) {
            instance = new Cart();
        }
        return instance;
    }

    public void loadUserCart(Context context, String userCode) {
        this.currentUserCode = userCode;
        SharedPreferences prefs = context.getSharedPreferences(PREFS_NAME, Context.MODE_PRIVATE);
        String json = prefs.getString(getCartKey(userCode), null);

        if (json != null) {
            try {
                Gson gson = new Gson();
                Type type = new TypeToken<ArrayList<Product>>(){}.getType();
                products = gson.fromJson(json, type);
            } catch (Exception e) {
                Log.e(TAG, "Error loading cart", e);
            }
        }

        if (products == null) {
            products = new ArrayList<>();
        }
    }

    public void saveCart(Context context) {
        if (currentUserCode != null && context != null) {
            SharedPreferences prefs = context.getSharedPreferences(PREFS_NAME, Context.MODE_PRIVATE);
            Gson gson = new Gson();
            String json = gson.toJson(products);
            prefs.edit().putString(getCartKey(currentUserCode), json).apply();
        }
    }

    public void addProduct(Product product, Context context) {
        products.add(product);
        saveCart(context);
    }

    public void removeProduct(Product product, Context context) {
        products.remove(product);
        saveCart(context);
    }

    public List<Product> getProducts() {
        return new ArrayList<>(products);
    }

    public double getTotalPrice() {
        double total = 0;
        for (Product p : products) {
            total += p.getPrice();
        }
        return total;
    }

    public void clearCart(Context context) {
        products.clear();
        saveCart(context);
    }

    private String getCartKey(String userCode) {
        return "cart_" + userCode;
    }

    public String getCurrentUserCode() {
        return currentUserCode;
    }
}

Product.java

package com.example.demo.models;

import java.io.Serializable;

public class Product implements Serializable {
    private String id;
    private String name;
    private double price;
    private String description;
    private int imageResId;

    public Product(String id, String name, double price, String description, int imageResId) {
        this.id = id;
        this.name = name;
        this.price = price;
        this.description = description;
        this.imageResId = imageResId;
    }

    // Геттеры
    public String getId() {
        return id;
    }

    public String getName() {
        return name;
    }

    public double getPrice() {
        return price;
    }

    public String getDescription() {
        return description;
    }

    public int getImageResId() {
        return imageResId;
    }

    // Сеттеры (если нужны)
    public void setId(String id) {
        this.id = id;
    }

    public void setName(String name) {
        this.name = name;
    }

    public void setPrice(double price) {
        this.price = price;
    }

    public void setDescription(String description) {
        this.description = description;
    }

    public void setImageResId(int imageResId) {
        this.imageResId = imageResId;
    }

    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (o == null || getClass() != o.getClass()) return false;
        Product product = (Product) o;
        return id.equals(product.id);
    }

    @Override
    public int hashCode() {
        return id.hashCode();
    }

    @Override
    public String toString() {
        return "Product{" +
                "id='" + id + '\'' +
                ", name='" + name + '\'' +
                ", price=" + price +
                '}';
    }
}

