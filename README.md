# parasolWeb

Run `npm run dev:ssr` for running this as server side app. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.


## Env variables needed
Run the parasol-store  parasol-db images locally and setup these URLs

export API_TRACK_USERACTIVITY="http://localhost:9000/track"
export API_GET_PAGINATED_PRODUCTS="https://parasol-store-parasol-user1.apps.sno.sandbox2137.opentlc.com/services/catalog/product"
export API_GET_PRODUCT_DETAILS_BY_IDS="http://parasol-store-parasol-user1.apps.sno.sandbox2137.opentlc.com/services/catalog/product/:ids" 
export API_CATALOG_RECOMMENDED_PRODUCT_IDS="http://localhost:9000/score/product"
export API_CART_SERVICE="http://localhost:9000/services/cart"
export API_CUSTOMER_SERVICE="http://localhost:9000/services/customer/id/:custId"
export API_ORDER_SERVICE="http://localhost:8080/web-gateway/services/order"

export SSO_CUSTOM_CONFIG="parasol-web-gateway"
export SSO_AUTHORITY="http://localhost:8180/realms/user1-parasol_users"
export SSO_REDIRECT_LOGOUT_URI="http://localhost:4200/home"
export SSO_LOG_LEVEL=2



## docker

podman build -t quay.io/redhat_pe_workshop/parasol-web:<tag> .
podman push quay.io/redhat_pe_workshop/parasol-web:<tag> 