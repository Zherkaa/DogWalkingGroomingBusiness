CREATE DATABASE DogWalkingGroomingBusiness;
USE DogWalkingGroomingBusiness;

CREATE TABLE Customer (
    CustomerID INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(100),
    PhoneNumber VARCHAR(15),
    Email VARCHAR(100),
    Address VARCHAR(255)
);

CREATE TABLE Pet (
    PetID INT AUTO_INCREMENT PRIMARY KEY,
    CustomerID INT,
    PetName VARCHAR(100),
    Breed VARCHAR(50),
    Age INT,
    HealthCondition VARCHAR(255),
    FOREIGN KEY (CustomerID) REFERENCES Customer(CustomerID)
);

CREATE TABLE Employee (
    EmployeeID INT AUTO_INCREMENT PRIMARY KEY,
    EmployeeName VARCHAR(100),
    Role VARCHAR(50),
    Schedule VARCHAR(255)
);

CREATE TABLE Service (
    ServiceID INT AUTO_INCREMENT PRIMARY KEY,
    ServiceType VARCHAR(50),
    Price DECIMAL(10,2),
    Description VARCHAR(50)
);

CREATE TABLE Appointment (
    AppointmentID INT AUTO_INCREMENT PRIMARY KEY,
    CustomerID INT,
    EmployeeID INT,
    ServiceID INT,
    AppointmentDateTime DATETIME,
    Status VARCHAR(50),
    FOREIGN KEY (CustomerID) REFERENCES Customer(CustomerID),
    FOREIGN KEY (EmployeeID) REFERENCES Employee(EmployeeID),
    FOREIGN KEY (ServiceID) REFERENCES Service(ServiceID)
);

CREATE TABLE Payment (
    PaymentID INT AUTO_INCREMENT PRIMARY KEY,
    AppointmentID INT,
    Amount DECIMAL(10,2),
    PaymentDate DATETIME,
    PaymentMethod VARCHAR(50),
    FOREIGN KEY (AppointmentID) REFERENCES Appointment(AppointmentID)
);

INSERT INTO Customer (Name, PhoneNumber, Email, Address) VALUES
('Zeynep Osman', '(917) 432-7845', 'ZeynepOsman@gmail.com', '752 E 95 st, NYC, NY'),
('Jane Smith', '(212) 456-7890', 'janesmith@yahoo.com', '456 Oak Ave, NYC, NY'),
('John Doe', '(646) 987-6543', 'johndoe@hotmail.com', '123 Main St, NYC, NY'),
('Bob Brown', '(917) 555-2345', 'bobbrown@gmail.com', '101 Maple Dr, NYC, NY'),
('Walter White', '(212) 555-3456', 'WalterWhite@outlook.com', '202 Birch Ln, NYC, NY'),
('Emily Davis', '(212) 123-4567', 'emilyd@gmail.com', '303 Cedar Blvd, NYC, NY');

INSERT INTO Employee (EmployeeName, Role, Schedule) VALUES
('Sarah Miller', 'Walker', 'Mon-Fri 9am-5pm'),
('Tim Williams', 'Groomer', 'Tue-Sat 10am-6pm'),
('George Harris', 'Walker', 'Mon-Wed 8am-4pm'),
('Rachel Green', 'Groomer', 'Wed-Sun 12pm-8pm'),
('Emma Lewis', 'Walker', 'Fri-Sun 9am-3pm');

INSERT INTO Pet (CustomerID, PetName, Breed, Age, HealthCondition) VALUES
(1, 'Luke', 'Golden Retriever', 3, 'Allergies (seasonal)'),
(1, 'Leia', 'Dalmation', 1, 'Healthy'),
(2, 'Daisy', 'Bulldog', 7, 'Arthritis'),
(3, 'Luna', 'Labrador', 2, 'Healthy'),
(3, 'Buddy', 'Golden Retriever', 2, 'Healthy'),
(4, 'Chico', 'Chihuahua', 11, 'Blind & Arthritis'),
(5, 'Rex', 'German Shepherd', 4, 'Healthy'),
(6, 'Bella', 'Beagle', 5, 'Healthy');

INSERT INTO Service (ServiceType, Price, Description) VALUES
('Dog Walking', 50.00, '60 mins'),
('Dog Walking', 65.00, '90 mins'),
('Dog Walking', 80.00, '120 mins'),
('Dog Grooming', 75.00, 'Hair Cut'),
('Dog Grooming', 20.00, 'Nails Clip'),
('Dog Grooming', 50.00, 'Wash'),
('Dog Grooming', 120.00, 'Full Service');

INSERT INTO Appointment (CustomerID, EmployeeID, ServiceID, AppointmentDateTime, Status) VALUES
(1, 1, 2, '2025-05-15 10:00:00', 'Scheduled'),
(2, 2, 3, '2025-05-16 14:00:00', 'Scheduled'),
(3, 3, 2, '2025-05-19 09:30:00', 'Scheduled'),
(4, 4, 3, '2025-05-21 13:00:00', 'Scheduled'),
(5, 1, 5, '2025-05-12 11:00:00', 'Completed'),
(6, 3, 7, '2025-05-22 16:30:00', 'Canceled');

INSERT INTO Payment (AppointmentID, Amount, PaymentDate, PaymentMethod) VALUES
(1, 65.00, '2025-05-13 10:30:00', 'Credit'),
(2, 80.00, '2025-05-12 14:30:00', 'Cash'),
(3, 65.00, '2025-05-14 10:00:00', 'Cash'),
(4, 80.00, '2025-05-14 14:00:00', 'Credit'),
(5, 20.00, '2025-05-16 11:30:00', 'Credit'),
(6, 0.00, '2025-05-13 17:00:00', 'CANCELED');

SELECT * FROM Customer;
SELECT * FROM Pet;
SELECT * FROM Employee;
SELECT * FROM Service;
SELECT * FROM Appointment;
SELECT * FROM Payment;
