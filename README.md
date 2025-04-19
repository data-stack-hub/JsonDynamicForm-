
# jsonDynamicForm

**A lightweight and flexible React form builder powered by JSON, React Hook Form, Zod, and ShadCN.**

[![npm](https://img.shields.io/npm/v/jsonDynamicForm.svg)](https://www.npmjs.com/package/jsonDynamicForm)
[![GitHub stars](https://img.shields.io/github/stars/your-username/jsonDynamicForm)](https://github.com/your-username/jsonDynamicForm/stargazers)
[![License](https://img.shields.io/github/license/your-username/jsonDynamicForm)](LICENSE)

---

## ✨ Features

- 📄 **JSON-based form configuration**
- ⚙️ **Built on React Hook Form**
- 🛡️ **Zod validation**
- 🎨 **Beautiful UI with ShadCN**
- 🔁 **Dynamic field rendering**
- 🧩 **Supports custom components**

---

## 🚀 Installation

```bash
npm install jsonDynamicForm react-hook-form zod
```

or

```bash
yarn add jsonDynamicForm react-hook-form zod
```

---

## 📦 Basic Usage

```tsx
import { JsonDynamicForm } from 'jsonDynamicForm';

const formSchema = {
  title: "User Info",
  fields: [
    {
      type: "text",
      name: "firstName",
      label: "First Name",
      required: true,
    },
    {
      type: "email",
      name: "email",
      label: "Email Address",
      required: true,
    },
    {
      type: "number",
      name: "age",
      label: "Age",
    },
  ],
};

export default function MyFormPage() {
  const handleSubmit = (data: any) => {
    console.log("Form Data:", data);
  };

  return <JsonDynamicForm schema={formSchema} onSubmit={handleSubmit} />;
}
```

---

## 📘 JSON Schema Format

```ts
interface JsonFormSchema {
  title?: string;
  fields: {
    name: string;
    type:
      | 'text'
      | 'number'
      | 'email'
      | 'password'
      | 'select'
      | 'checkbox'
      | 'radio'
      | 'textarea';
    label: string;
    required?: boolean;
    options?: { label: string; value: any }[]; // for select, radio
    defaultValue?: any;
    placeholder?: string;
  }[];
}
```

---

## 💡 Roadmap

- [x] JSON field schema support
- [x] Zod validation
- [x] Integrate with ShadCN components
- [ ] Custom field renderer support
- [ ] Conditional fields
- [ ] Grouped sections
- [ ] Async data for select fields
- [ ] Drag-and-drop form builder (future)
- [ ] Playground & UI config editor

---

## 🛠️ Contributing

We welcome contributions! Please check the [CONTRIBUTING.md](CONTRIBUTING.md) for how to get started.

To run the project locally:

```bash
git clone https://github.com/your-username/jsonDynamicForm.git
cd jsonDynamicForm
npm install
npm run dev
```

---

## 📄 License

MIT © [Your Name](https://github.com/your-username)
