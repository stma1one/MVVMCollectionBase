# Toy Store MVVM Sample

This project is a .NET MAUI application that demonstrates the MVVM (Model-View-ViewModel) pattern in a toy store context. The application allows users to view, filter, and manage a collection of toys.

## Project Structure

The project is organized into several key components:

- **Views**: Contains the XAML files for the user interface.
  - 'AddToyPage.xaml': Page to add a new toy (currently not added to any List)
  - `ViewToysPage.xaml`: The main page for displaying the list of toys.

- **ViewModels**: Contains the view models that handle the business logic and data presentation.
  - `ViewToysPageViewModel.cs`: Manages the data and operations for the ViewToysPage.
  - 'AddToysPageViewModel.cs': Manages the data and operations for the AddToyPage.
  - `ViewModelBase.cs`: A base class for view models that implements `INotifyPropertyChanged`.
    

- **Models**: Contains the data models used in the application.
  - `Toy.cs`: Represents a toy item.
  - 'ToyTypes.cs': Represents a toy types.

- **Services**: Contains classes that handle data operations.
  - `ToyService.cs`: Manages the collection of toys and provides methods for filtering and manipulating the data.

## Features

1. **View Toys**: Displays a list of toys with their images, names, and prices.
2. **Price Filtering**: Allows users to filter toys above or below a specified price.
3. **Refresh**: Users can refresh the list of toys.
4. **Delete Toy**: Swipe-to-delete functionality for removing toys from the list.
5. **Localization**: The UI text is in Hebrew, indicating support for right-to-left languages.

## Key Components

### ViewToysPage (View)

- Uses a `CollectionView` to display the list of toys.
- Implements a `SwipeView` for delete functionality.
- Uses `RefreshView` for pull-to-refresh capability.
- Contains UI elements for price filtering.

### ViewToysPageViewModel (ViewModel)

- Manages the `ObservableCollection<Toy>` that populates the UI.
- Implements commands for refreshing, filtering, and deleting toys.
- Utilizes `ToyService` for data operations.

### ToyService (Service)

- Implements the `IToys` interface.
- Provides methods for retrieving, filtering, adding, and deleting toys.
- Currently uses in-memory data, but can be extended to use a database or API.

## Getting Started

To run this project:

1. Ensure you have the .NET MAUI development environment set up.
2. Clone the repository.
3. Open the solution in Visual Studio.
4. Build and run the project on your desired platform (iOS, Android, Windows, or macOS).

## Future Enhancements

- Implement persistent storage for toys (e.g., database integration).
- Add functionality to add new toys through the UI to the DB.
- Implement sorting options for the toy list.


## Contributing

This is for learning purpose only.

## License

Free to use. 
