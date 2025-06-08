# TaskFlow .NET

A modern, full-stack task management web application built with ASP.NET Core and Entity Framework. Clean, functional, and production-ready.

## 🚀 Live Demo

[View Live Application](your-deployment-url-here)

## ✨ Features

- **User Authentication**: Secure registration and login system
- **Task Management**: Create, edit, delete, and organize tasks
- **Deadline Tracking**: Set and monitor task deadlines with visual indicators
- **Priority Levels**: Organize tasks by importance (High, Medium, Low)
- **Status Tracking**: Mark tasks as To-Do, In Progress, or Completed
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Real-time Updates**: Dynamic UI updates without page refreshes

## 🛠️ Tech Stack

- **Backend**: ASP.NET Core 8.0
- **Database**: Entity Framework Core with SQL Server
- **Frontend**: Razor Pages with Bootstrap 5
- **Authentication**: ASP.NET Core Identity
- **Deployment**: Azure App Service
- **Testing**: xUnit with Moq

## 📋 Prerequisites

- .NET 8.0 SDK
- SQL Server (LocalDB for development)
- Visual Studio 2022 or VS Code

## 🔧 Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/taskflow-dotnet.git
   cd taskflow-dotnet
   ```

2. **Restore dependencies**
   ```bash
   dotnet restore
   ```

3. **Update database connection string**
   ```json
   // appsettings.json
   {
     "ConnectionStrings": {
       "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=TaskFlowDb;Trusted_Connection=true;MultipleActiveResultSets=true"
     }
   }
   ```

4. **Apply database migrations**
   ```bash
   dotnet ef database update
   ```

5. **Run the application**
   ```bash
   dotnet run
   ```

6. **Open browser to** `https://localhost:7001`

## 📊 Database Schema

```sql
Users
├── Id (Primary Key)
├── Email
├── PasswordHash
└── CreatedAt

Tasks
├── Id (Primary Key)
├── Title
├── Description
├── Priority (Enum)
├── Status (Enum)
├── DueDate
├── CreatedAt
├── UpdatedAt
└── UserId (Foreign Key)
```

## 🧪 Testing

Run the test suite:
```bash
dotnet test
```

Test coverage includes:
- Unit tests for business logic
- Integration tests for API endpoints
- Database repository tests

## 🚀 Deployment

### Azure Deployment
1. Create Azure App Service and SQL Database
2. Configure connection strings in Azure portal
3. Deploy using Visual Studio or Azure CLI:
   ```bash
   az webapp deployment source config-zip --resource-group myResourceGroup --name myAppName --src release.zip
   ```

### Docker Deployment
```bash
docker build -t taskflow-dotnet .
docker run -p 8080:80 taskflow-dotnet
```

## 📁 Project Structure

```
TaskFlow/
├── Controllers/          # MVC Controllers
├── Models/              # Data models and ViewModels
├── Views/               # Razor views
├── Data/                # Entity Framework context
├── Services/            # Business logic services
├── wwwroot/             # Static files (CSS, JS, images)
├── Migrations/          # EF Core migrations
└── Tests/               # Unit and integration tests
```

## 🎯 Key Implementation Highlights

- **Clean Architecture**: Separation of concerns with proper layering
- **Security**: Input validation, CSRF protection, secure password hashing
- **Performance**: Async/await patterns, efficient database queries
- **Error Handling**: Global exception handling with user-friendly messages
- **Logging**: Structured logging with Serilog

## 📈 Future Enhancements

- [ ] Task categories and tags
- [ ] Team collaboration features
- [ ] File attachments
- [ ] Mobile app with Xamarin
- [ ] Integration with calendar applications
- [ ] Advanced reporting and analytics

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Your Name**
- GitHub: [@yourusername](https://github.com/yourusername)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/yourprofile)
- Email: your.email@example.com

---

⭐ If you found this project helpful, please give it a star!