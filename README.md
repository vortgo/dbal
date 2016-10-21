# Doctrine DBAL for laravel migrations

## Changed files from original package
dbal/lib/Doctrine/DBAL/Schema/Column.php

dbal/lib/Doctrine/DBAL/Types/EnumType.php

## Usage

When you need changing field enum, just added in your migrations file

Doctrine\DBAL\Types\Type::addType('enum', 'Doctrine\DBAL\Types\EnumType');  

Schema::getConnection()->getDoctrineSchemaManager()->getDatabasePlatform()->registerDoctrineTypeMapping('enum', 'string');
