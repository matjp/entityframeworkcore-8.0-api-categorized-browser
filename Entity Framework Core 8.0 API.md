Microsoft.EntityFrameworkCore

<details>
<summary>Change Tracker</summary>

* Classes
  * `ChangeTrackerExtensions` - Extension methods for ChangeTracker.
* Enums
  * `ChangeTrackingStrategy` - Indicates how the context detects changes to properties for an instance of the entity type.
* Namespaces
  * [`Microsoft.EntityFrameworkCore.ChangeTracking`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.changetracking?view=efcore-8.0)

</details>

<details>
<summary>Convention Entity Type</summary>

* Classes
  * `ConventionEntityTypeExtensions` - Extension methods for IConventionEntityType.

</details>

<details>
<summary>Cosmos</summary>

* Classes
  * `CosmosDatabaseFacadeExtensions` - Extension methods for the DatabaseFacade returned from Database that can be used only with the Cosmos provider.
  * `CosmosDbContextOptionsExtensions` - Cosmos-specific extension methods for DbContextOptionsBuilder.
  * `CosmosEntityTypeBuilderExtensions` - Cosmos-specific extension methods for EntityTypeBuilder.
  * `CosmosEntityTypeExtensions` - Entity type extension methods for Cosmos metadata.
  * `CosmosModelBuilderExtensions` - Cosmos-specific extension methods for ModelBuilder.
  * `CosmosModelExtensions` - Model extension methods for Cosmos metadata.
  * `CosmosPrimitiveCollectionBuilderExtensions` - Cosmos-specific extension methods for PrimitiveCollectionBuilder.
  * `CosmosPropertyBuilderExtensions` - Cosmos-specific extension methods for PropertyBuilder.
  * `CosmosPropertyExtensions` - Property extension methods for Cosmos metadata.
  * `CosmosQueryableExtensions` - Cosmos-specific extension methods for LINQ queries.
* Namespaces
  * [`Microsoft.EntityFrameworkCore.Cosmos.Metadata.Conventions`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.cosmos.metadata.conventions?view=efcore-8.0)

</details>

<details>
<summary>Database Context</summary>

* Classes
  * `DbContext` - A DbContext instance represents a session with the database and can be used to query and save instances of your entities. DbContext is a combination of the Unit Of Work and Repository patterns.
  * `DbContextOptions` - The options to be used by a DbContext. You normally override OnConfiguring(DbContextOptionsBuilder) or use a DbContextOptionsBuilder to create instances of this class and it is not designed to be directly constructed in your application code.
  * `DbContextOptions<TContext>` - The options to be used by a DbContext. You normally override OnConfiguring(DbContextOptionsBuilder) or use a DbContextOptionsBuilder<TContext> to create instances of this class and it is not designed to be directly constructed in your application code.
  * `DbContextOptionsBuilder` - Provides a simple API surface for configuring DbContextOptions. Databases (and other extensions) typically define extension methods on this object that allow you to configure the database connection (and other options) to be used for a context.
  * `DbContextOptionsBuilder<TContext>` - Provides a simple API surface for configuring DbContextOptions<TContext>. Databases (and other extensions) typically define extension methods on this object that allow you to configure the database connection (and other options) to be used for a context.
* Structs
  * `DbContextId` - A unique identifier for the context instance and pool lease, if any.
* Interfaces
  * `IDbContextFactory<TContext>` - Defines a factory for creating DbContext instances.

</details>

<details>
<summary>Database Functions</summary>

* Attributes
  * `DbFunctionAttribute` - Maps a static CLR method to a database function so that the CLR method may be used in LINQ queries. By convention uses the .NET method name as name of the database function and the default schema.
* Classes
  * `DbFunctions` - Provides CLR methods that get translated to database functions when used in LINQ to Entities queries. The methods on this class are accessed via Functions.
  * `DbFunctionsExtensions` - Provides CLR methods that get translated to database functions when used in LINQ to Entities queries. The methods on this class are accessed via Functions.

</details>

<details>
<summary>Database Logger Category</summary>

* Classes
  * `DbLoggerCategory` - An API for getting logger categories in an Intellisense/tab-completion friendly manner.
  * `DbLoggerCategory.ChangeTracking` - Logger category for messages from change detection and tracking.
  * `DbLoggerCategory.Database` - Logger categories for messages related to database interactions.
  * `DbLoggerCategory.Database.Command` - Logger category for command execution, including SQL sent to the database.
  * `DbLoggerCategory.Database.Connection` - Logger category for messages related to connection operations.
  * `DbLoggerCategory.Database.Transaction` - Logger category for messages related to transaction operations.
  * `DbLoggerCategory.Infrastructure` - Logger category for miscellaneous messages from the Entity Framework infrastructure.
  * `DbLoggerCategory.Migrations` - Logger category messages from Migrations.
  * `DbLoggerCategory.Model` - Logger categories for messages related to model building and metadata.
  * `DbLoggerCategory.Model.Validation` - Logger category for messages from model validation.
  * `DbLoggerCategory.Query` - Logger category for messages related to queries, excluding the generated SQL, which is in the DbLoggerCategory.Database.Command category.
  * `DbLoggerCategory.Scaffolding` - Logger category for messages from scaffolding/reverse engineering.
  * `DbLoggerCategory.Update` - Logger category for messages related to SaveChanges(), excluding messages specifically relating to database interactions which are covered by the DbLoggerCategory.Database categories.

</details>

<details>
<summary>DbSet</summary>

* Classes
  * `DbSet<TEntity>` - A DbSet<TEntity> can be used to query and save instances of TEntity. LINQ queries against a DbSet<TEntity> will be translated into queries against the database.

</details>

<details>
<summary>Dependency Injection</summary>

* Namespaces
  * [`Microsoft.Extensions.DependencyInjection`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.dependencyinjection?view=efcore-8.0)

</details>

<details>
<summary>Design</summary>

* Namespaces
  * [`Microsoft.EntityFrameworkCore.Design`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.design?view=efcore-8.0)

</details>

<details>
<summary>Diagnostics</summary>

* Namespaces
  * [`Microsoft.EntityFrameworkCore.Diagnostics`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.diagnostics?view=efcore-8.0)

</details>

<details>
<summary>Entity Framework</summary>

* Attributes
  * `BackingFieldAttribute` - Names the backing field associated with this property or navigation property.
  * `CommentAttribute` - Marks a class, property or field with a comment to be set on the corresponding database table or column.
  * `DeleteBehaviorAttribute` - Configures the navigation property on the dependent side of a relationship to indicate how a delete operation is applied to dependent entities in a relationship when it is deleted or the relationship is severed.
  * `IndexAttribute` - Specifies an index to be generated in the database.
  * `KeylessAttribute` - Marks a type as keyless entity.
  * `OwnedAttribute` - Marks a type as owned. All references to this type will be configured as owned entity types.
  * `PrecisionAttribute` - Configures the precision of data that is allowed in this property. For example, if the property is a Decimal then this is the maximum number of digits.
  * `PrimaryKeyAttribute` - Specifies a primary key for the entity type mapped to this CLR type.
  * `UnicodeAttribute` - Configures the property as capable of persisting unicode characters.
* Classes
  * `EF` - Static methods that are useful in application code where there is not an EF type for the method to be accessed from. For example, referencing a shadow state property in a LINQ query.
  * `EntityFrameworkQueryableExtensions` - Entity Framework LINQ related extension methods.
* Enums
  * `AutoTransactionBehavior` - Indicates whether or not a transaction will be created automatically by SaveChanges() if a user transaction wasn't created via 'BeginTransaction' or provided via 'UseTransaction'.
  * `DataCompressionType` - Indicates type of data compression used on a index.
  * `DeleteBehavior` - Indicates how a delete operation is applied to dependent entities in a relationship when the principal is deleted or the relationship is severed.
  * `EntityState` - The state in which an entity is being tracked by a context.
  * `PropertyAccessMode` - Pass a value from this enum to UsePropertyAccessMode(PropertyAccessMode), UsePropertyAccessMode(PropertyAccessMode), or UsePropertyAccessMode(PropertyAccessMode) to change whether the property or backing field will be used when reading and writing to a property or field.
  * `QuerySplittingBehavior` - Indicates how the related collections in a query should be loaded from database.
  * `QueryTrackingBehavior` - Indicates how the results of a query are tracked by the ChangeTracker.
  * `WarningBehavior` - The runtime behavior of warnings generated by Entity Framework

</details>

<details>
<summary>Entity Type</summary>

* Attributes
  * `EntityTypeConfigurationAttribute` - Specifies the configuration type for the entity type.
  * `EntityTypeConfigurationAttribute<TConfiguration,TEntity>` - Specifies the configuration type for the entity type.
* Classes
  * `EntityTypeExtensions` - Entity type extension methods for IReadOnlyEntityType.
* Interfaces
  * `IEntityTypeConfiguration<TEntity>` - Allows configuration for an entity type to be factored into a separate class, rather than in-line in OnModelCreating(ModelBuilder). Implement this interface, applying configuration for the entity in the Configure(EntityTypeBuilder<TEntity>) method, and then apply the configuration to the model using ApplyConfiguration<TEntity>(IEntityTypeConfiguration<TEntity>) in OnModelCreating(ModelBuilder).

</details>

<details>
<summary>Execution Strategy</summary>

* Classes
  * `ExecutionStrategyExtensions` - Extension methods for IExecutionStrategy

</details>

<details>
<summary>In-Memory</summary>

* Classes
  * `InMemoryDatabaseFacadeExtensions` - In-memory specific extension methods for Database.
  * `InMemoryDbContextOptionsExtensions` - In-memory specific extension methods for DbContextOptionsBuilder.
  * `InMemoryEntityTypeBuilderExtensions` - Extension methods for EntityTypeBuilder for the in-memory provider.
  * `InMemoryEntityTypeExtensions` - Extension methods for IReadOnlyEntityType for the in-memory provider.
* Namespaces
  * [`Microsoft.EntityFrameworkCore.InMemory.Metadata.Conventions`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.inmemory.metadata.conventions?view=efcore-8.0)

</details>

<details>
<summary>Infrastructure</summary>

* Namespaces
  * [`Microsoft.EntityFrameworkCore.Infrastructure`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.infrastructure?view=efcore-8.0)

</details>

<details>
<summary>Lazy Loading</summary>

* Classes
  * `LazyLoadingProxiesOptionsBuilder` - Allows SQL Server specific configuration to be performed on DbContextOptions.

</details>

<details>
<summary>Metadata</summary>

* Namespaces
  * [`Microsoft.EntityFrameworkCore.Metadata`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.metadata?view=efcore-8.0)
  * [`Microsoft.EntityFrameworkCore.Metadata.Builders`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.metadata.builders?view=efcore-8.0)
  * [`Microsoft.EntityFrameworkCore.Metadata.Conventions`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.metadata.conventions?view=efcore-8.0)
  * [`Microsoft.EntityFrameworkCore.Metadata.Conventions.Infrastructure`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.metadata.conventions.infrastructure?view=efcore-8.0)

</details>

<details>
<summary>Migrations</summary>

* Namespaces
  * [`Microsoft.EntityFrameworkCore.Migrations`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.migrations?view=efcore-8.0)
  * [`Microsoft.EntityFrameworkCore.Migrations.Design`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.migrations.design?view=efcore-8.0)
  * [`Microsoft.EntityFrameworkCore.Migrations.Operations`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.migrations.operations?view=efcore-8.0)
  * [`Microsoft.EntityFrameworkCore.Migrations.Operations.Builders`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.migrations.operations.builders?view=efcore-8.0)

</details>

<details>
<summary>Model</summary>

* Classes
  * `ModelBuilder` - Provides a simple API surface for configuring a IMutableModel that defines the shape of your entities, the relationships between them, and how they map to the database.
  * `ModelConfigurationBuilder` - Provides a simple API surface for setting defaults and configuring conventions before they run.
  * `ModelCreationDependencies` - This is an internal API that supports the Entity Framework Core infrastructure and not subject to the same compatibility standards as public APIs. It may be changed or removed without notice in any release. You should only use it directly in your code with extreme caution and knowing that doing so can result in application failures when updating to a new Entity Framework Core release.

</details>

<details>
<summary>Mutable Entity Type</summary>

* Classes
  * `MutableEntityTypeExtensions` - Extension methods for IMutableEntityType.

</details>

<details>
<summary>Observable Collection</summary>

* Classes
  * `ObservableCollectionExtensions` - Extension methods for ObservableCollection<T>.

</details>

<details>
<summary>Property Base</summary>

* Classes
  * `PropertyBaseExtensions` - Extension methods for IReadOnlyPropertyBase.

</details>

<details>
<summary>Proxies</summary>

* Classes
  * `ProxiesExtensions` - Extension methods related to use of proxies with Entity Framework Core.

</details>

<details>
<summary>Query</summary>

* Namespaces
  * [`Microsoft.EntityFrameworkCore.Query`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.query?view=efcore-8.0)
  * [`Microsoft.EntityFrameworkCore.Query.SqlExpressions`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.query.sqlexpressions?view=efcore-8.0)

</details>

<details>
<summary>Relational Database</summary>

* Classes
  * `RelationalComplexTypeExtensions` - Complex type extension methods for relational database metadata.
  * `RelationalComplexTypePrimitiveCollectionBuilderExtensions` - Relational database specific extension methods for ComplexTypePrimitiveCollectionBuilder.
  * `RelationalComplexTypePropertyBuilderExtensions` - Relational database specific extension methods for ComplexTypePropertyBuilder.
  * `RelationalDatabaseFacadeExtensions` - Extension methods for the DatabaseFacade returned from Database that can be used only with relational database providers.
  * `RelationalDbFunctionsExtensions` - Provides CLR methods that get translated to database functions when used in LINQ to Entities queries. The methods on this class are accessed via Functions.
  * `RelationalElementTypeBuilderExtensions` - Relational database specific extension methods for ElementTypeBuilder.
  * `RelationalElementTypeExtensions` - IElementType extension methods for relational database metadata.
  * `RelationalEntityTypeBuilderExtensions` - Relational database specific extension methods for EntityTypeBuilder.
  * `RelationalEntityTypeExtensions` - Entity type extension methods for relational database metadata.
  * `RelationalForeignKeyBuilderExtensions` - Relational database specific extension methods for relationship builders.
  * `RelationalForeignKeyExtensions` - Foreign key extension methods for relational database metadata.
  * `RelationalIndexBuilderExtensions` - Relational database specific extension methods for IndexBuilder.
  * `RelationalIndexExtensions` - Index extension methods for relational database metadata.
  * `RelationalKeyBuilderExtensions` - Relational database specific extension methods for KeyBuilder.
  * `RelationalKeyExtensions` - Key extension methods for relational database metadata.
  * `RelationalModelBuilderExtensions` - Relational database specific extension methods for ModelBuilder.
  * `RelationalModelExtensions` - Relational-specific model extension methods.
  * `RelationalOwnedNavigationBuilderExtensions` - Relational database specific extension methods for OwnedNavigationBuilder.
  * `RelationalPrimitiveCollectionBuilderExtensions` - Relational database specific extension methods for PrimitiveCollectionBuilder.
  * `RelationalPropertiesConfigurationBuilderExtensions` - Relational database specific extension methods for PropertiesConfigurationBuilder.
  * `RelationalPropertyBuilderExtensions` - Relational database specific extension methods for PropertyBuilder.
  * `RelationalPropertyExtensions` - Property extension methods for relational database metadata.
  * `RelationalQueryableExtensions` - Relational database specific extension methods for LINQ queries.
  * `RelationalTriggerBuilderExtensions` - Relational database specific extension methods for TriggerBuilder.
  * `RelationalTriggerExtensions` - Trigger extension methods for relational database metadata.
  * `RelationalTypeBaseExtensions` - Type extension methods for relational database metadata.
  * `RelationalTypeMappingConfigurationBuilderExtensions` - Relational database specific extension methods for TypeMappingConfigurationBuilder.

</details>

<details>
<summary>Save Changes Arguments</summary>

* Classes
  * `SaveChangesEventArgs` - Base event arguments for the DbContext.SaveChanges and DbContext.SaveChangesAsync events.
  * `SaveChangesFailedEventArgs` - Event arguments for the SaveChangesFailed event.
  * `SavedChangesEventArgs` - Event arguments for the SavedChanges event.
  * `SavingChangesEventArgs` - Event arguments for the SavingChanges event.

</details>

<details>
<summary>Scaffolding</summary>

* Classes
  * `ScaffoldingModelExtensions` - Design-time model extensions.
* Namespaces
  * [`Microsoft.EntityFrameworkCore.Scaffolding`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.scaffolding?view=efcore-8.0)
  * [`Microsoft.EntityFrameworkCore.Scaffolding.Metadata`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.scaffolding.metadata?view=efcore-8.0)

</details>

<details>
<summary>Sqlite</summary>

* Classes
  * `SqliteComplexTypePropertyBuilderExtensions` - SQLite-specific extension methods for ComplexTypePropertyBuilder.
  * `SqliteDatabaseFacadeExtensions` - SQLite specific extension methods for Database.
  * `SqliteDbContextOptionsBuilderExtensions` - SQLite specific extension methods for DbContextOptionsBuilder.
  * `SqliteDbFunctionsExtensions` - Contains extension methods on DbFunctions for the Microsoft.EntityFrameworkCore.Sqlite provider.
  * `SqliteEntityTypeExtensions` - Entity type extension methods for Sqlite-specific metadata.
  * `SqliteEntityTypeMappingFragmentExtensions` - SQLite specific extension methods for IReadOnlyEntityTypeMappingFragment.
  * `SqliteNetTopologySuiteDbContextOptionsBuilderExtensions` - NetTopologySuite specific extension methods for SqliteDbContextOptionsBuilder.
  * `SqlitePropertyBuilderExtensions` - SQLite-specific extension methods for PropertyBuilder.
  * `SqlitePropertyExtensions` - Extension methods for IProperty for SQLite metadata.
  * `SqliteTableBuilderExtensions` - Sqlite-specific extension methods for TableBuilder.
  * `SqliteTableExtensions` - SQLite specific extension methods for ITable.
* Namespaces
  * [`Microsoft.EntityFrameworkCore.Sqlite.Query.SqlExpressions.Internal`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.sqlite.query.sqlexpressions.internal?view=efcore-8.0)
  * [`Microsoft.EntityFrameworkCore.Sqlite.Storage.Json`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.sqlite.storage.json?view=efcore-8.0)
  * [`Microsoft.EntityFrameworkCore.Sqlite.Storage.Json.Internal`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.sqlite.storage.json.internal?view=efcore-8.0)

</details>

<details>
<summary>Sql Server</summary>

* Classes
  * `SqlServerComplexTypePrimitiveCollectionBuilderExtensions` - SQL Server specific extension methods for ComplexTypePrimitiveCollectionBuilder.
  * `SqlServerComplexTypePropertyBuilderExtensions` - SQL Server specific extension methods for ComplexTypePropertyBuilder.
  * `SqlServerDatabaseFacadeExtensions` - SQL Server specific extension methods for Database.
  * `SqlServerDbContextOptionsExtensions` - SQL Server specific extension methods for DbContextOptionsBuilder.
  * `SqlServerDbFunctionsExtensions` - Provides CLR methods that get translated to database functions when used in LINQ to Entities queries. The methods on this class are accessed via Functions.
  * `SqlServerDbSetExtensions` - Sql Server database specific extension methods for LINQ queries rooted in DbSet.
  * `SqlServerEntityTypeBuilderExtensions` - SQL Server specific extension methods for EntityTypeBuilder.
  * `SqlServerEntityTypeExtensions` - Entity type extension methods for SQL Server-specific metadata.
  * `SqlServerEntityTypeMappingFragmentExtension` - SQL Server specific extension methods for IReadOnlyEntityTypeMappingFragment.
  * `SqlServerIndexBuilderExtensions` - SQL Server specific extension methods for IndexBuilder.
  * `SqlServerIndexExtensions` - Index extension methods for SQL Server-specific metadata.
  * `SqlServerKeyBuilderExtensions` - SQL Server specific extension methods for KeyBuilder.
  * `SqlServerKeyExtensions` - Key extension methods for SQL Server-specific metadata.
  * `SqlServerModelBuilderExtensions` - SQL Server specific extension methods for ModelBuilder.
  * `SqlServerModelExtensions` - Model extension methods for SQL Server-specific metadata.
  * `SqlServerPrimitiveCollectionBuilderExtensions` - SQL Server specific extension methods for PrimitiveCollectionBuilder.
  * `SqlServerPropertyBuilderExtensions` - SQL Server specific extension methods for PropertyBuilder.
  * `SqlServerPropertyExtensions` - Property extension methods for SQL Server-specific metadata.
  * `SqlServerRetryingExecutionStrategy` - An IExecutionStrategy implementation for retrying failed executions on SQL Server.
  * `SqlServerTableBuilderExtensions` - SQL Server specific extension methods for TableBuilder.
  * `SqlServerTableExtensions` - SQL Server specific extension methods for ITable.

</details>

<details>
<summary>Storage</summary>

* Namespaces
  * [`Microsoft.EntityFrameworkCore.Storage`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.storage?view=efcore-8.0)
  * [`Microsoft.EntityFrameworkCore.Storage.Json`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.storage.json?view=efcore-8.0)
  * [`Microsoft.EntityFrameworkCore.Storage.ValueConversion`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.storage.valueconversion?view=efcore-8.0)

</details>

<details>
<summary>Table Expressions</summary>

* Classes
  * `TableExpressionExtensions` - Type extension methods for TableExpressionBase and related types.

</details>

<details>
<summary>Transactions</summary>

* Namespaces
  * [`System.Transactions`](https://learn.microsoft.com/en-us/dotnet/api/system.transactions?view=efcore-8.0)

</details>

<details>
<summary>Update</summary>

* Exception Classes
  * `DbUpdateConcurrencyException` - An exception that is thrown when a concurrency violation is encountered while saving to the database. A concurrency violation occurs when an unexpected number of rows are affected during save. This is usually because the data in the database has been modified since it was loaded into memory.
  * `DbUpdateException` - An exception that is thrown when an error is encountered while saving to the database.
* Namespaces
  * [`Microsoft.EntityFrameworkCore.Update`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.update?view=efcore-8.0)

</details>

<details>
<summary>Value Generation</summary>

* Namespaces
  * [`Microsoft.EntityFrameworkCore.ValueGeneration`](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.valuegeneration?view=efcore-8.0)

</details>
