# Multi-tenancy Migration Steps
1. **Run Migrations**
   - `php artisan migrate`
2. **Create Tenant**
   - Login using super-admin account through PM
   - Keep the tenant domain as same of your FE host - you can get this from the network tabs **request headers host name**.
   - Create new tenant from PM request
   - A tenant should be created in your tenants table.
3. **Assign Tenant ID**
   - `php artisan assign:tenant-id {tenant_id}`
   - Replace {tenant_id} with actual ID
4. **Resume Operations**
   - Tenant users can login normally
   - System is ready for multi-tenant use
   - You can now login normally with your existing accounts.
  
# Fresh Database Setup
1. **Setup Database**
   - Run migrations and seeders: `php artisan migrate --seed`

2. **Access System**
   - Login with superadmin credentials

3. **Create Tenants**
   - Create tenants via PM collection with the admin accounts info
   - Tenant admin user would get email to reset there passowrd
   - Tenant Users can then login with their credentials after resetting their passwords
