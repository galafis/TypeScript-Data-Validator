# TypeScript-Data-Validator

## 🖼️ Hero Image

![TypeScript Data Validator Hero Image](hero_image.png)

## English

### Advanced Data Validation Framework

This project presents a robust and flexible data validation framework built with TypeScript. It ensures type safety and data integrity across various applications, providing developers with powerful tools to define and enforce data schemas.

### Features

*   **Type-Safe Validation:** Leverage TypeScript's powerful type system for compile-time and runtime validation.
*   **Flexible Schema Definition:** Define complex data structures with ease using a declarative API.
*   **Customizable Validators:** Extend the framework with custom validation rules to fit specific business logic.
*   **Detailed Error Reporting:** Receive clear and actionable error messages for failed validations.
*   **High Performance:** Optimized for efficiency, ensuring minimal overhead in critical applications.

### Quick Start

To get started with TypeScript-Data-Validator, follow these steps:

```bash
npm install && npm run build && npm start
```

### Usage Example

```typescript
import { Validator, Schema } from 'typescript-data-validator';

interface User {
  id: number;
  name: string;
  email: string;
  age?: number;
}

const userSchema: Schema<User> = {
  id: { type: 'number', required: true },
  name: { type: 'string', required: true, minLength: 3 },
  email: { type: 'string', required: true, format: 'email' },
  age: { type: 'number', optional: true, min: 18 },
};

const validator = new Validator(userSchema);

const validUser = { id: 1, name: 'Gabriel', email: 'gabriel@example.com', age: 30 };
const invalidUser = { id: '2', name: 'Jo', email: 'invalid-email', age: 15 };

console.log('Valid User:', validator.validate(validUser)); // { success: true, data: validUser }
console.log('Invalid User:', validator.validate(invalidUser)); // { success: false, errors: [...] }
```

## Português

### Estrutura Avançada de Validação de Dados

Este projeto apresenta uma estrutura de validação de dados robusta e flexível, construída com TypeScript. Ele garante a segurança de tipos e a integridade dos dados em diversas aplicações, fornecendo aos desenvolvedores ferramentas poderosas para definir e aplicar esquemas de dados.

### Funcionalidades

*   **Validação com Segurança de Tipo:** Aproveite o poderoso sistema de tipos do TypeScript para validação em tempo de compilação e execução.
*   **Definição de Esquema Flexível:** Defina estruturas de dados complexas com facilidade usando uma API declarativa.
*   **Validadores Personalizáveis:** Estenda a estrutura com regras de validação personalizadas para se adequar à lógica de negócios específica.
*   **Relatório de Erros Detalhado:** Receba mensagens de erro claras e acionáveis para validações falhas.
*   **Alto Desempenho:** Otimizado para eficiência, garantindo sobrecarga mínima em aplicações críticas.

### Início Rápido

Para começar a usar o TypeScript-Data-Validator, siga estes passos:

```bash
npm install && npm run build && npm start
```

### Exemplo de Uso

```typescript
import { Validator, Schema } from 'typescript-data-validator';

interface User {
  id: number;
  name: string;
  email: string;
  age?: number;
}

const userSchema: Schema<User> = {
  id: { type: 'number', required: true },
  name: { type: 'string', required: true, minLength: 3 },
  email: { type: 'string', required: true, format: 'email' },
  age: { type: 'number', optional: true, min: 18 },
};

const validator = new Validator(userSchema);

const validUser = { id: 1, name: 'Gabriel', email: 'gabriel@example.com', age: 30 };
const invalidUser = { id: '2', name: 'Jo', email: 'invalid-email', age: 15 };

console.log('Valid User:', validator.validate(validUser)); // { success: true, data: validUser }
console.log('Invalid User:', validator.validate(invalidUser)); // { success: false, errors: [...] }
```

## Author
Gabriel Demetrios Lafis

