# Local Storage Qollanba

## 1. Local Storage Nizamlari

Local Storage - veb brauzerda mag'liwmatlardi saqlaw ushin JavaScript APIs.

### Mumkinshilikler:
- Brauzer yadinda mag'liwmat uzaq saqlanadi
- Domen ishinda mag'liwmat saqlanadi
- Maksimal 5-10 MB yad

## 2. Tiykargi Operatsiyalar

### mag'liwmat Saqlaw
```javascript
localStorage.setItem('username', 'NawayiyNomi');
const user = { name: 'Alisher', age: 25 };
localStorage.setItem('user', JSON.stringify(user));
```

### mag'liwmat Oqiw
```javascript
const username = localStorage.getItem('username');
const savedUser = JSON.parse(localStorage.getItem('user'));
```

### mag'liwmat Oshiriw
```javascript
localStorage.removeItem('username');
localStorage.clear();
```

## 3. Todo Proyekt Misalinda
```javascript
class TodoManager {
    constructor() {
        this.todos = JSON.parse(localStorage.getItem('todos')) || [];
    }

    addTodo(todo) {
        this.todos.push(todo);
        localStorage.setItem('todos', JSON.stringify(this.todos));
    }
}
```

## 4. Diqqatqa Aliw kerek bolgan narseler
- Tek string formatda saqlanadi
- Domen boyinsha sheklengen
- Sinxronli operatsiya

## 5. Brauzer Qollaw Tekseriw
```javascript
if (typeof(Storage) !== "undefined") {
    console.log("Local Storage qollaydı");
} else {
    console.log("Local Storage qollamaydi");
}
```
