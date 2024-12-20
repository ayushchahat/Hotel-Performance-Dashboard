# Hotel Performance Data Analysis

This project involves analyzing and visualizing hotel performance data using multiple datasets. The provided datasets contain detailed information about dates, hotels, rooms, bookings, and revenue. Below is a description of the CSV files and their columns.

---

## Table of Contents
1. [Datasets](#datasets)
2. [Column Descriptions](#column-descriptions)
   - [dim_date](#dim_date)
   - [dim_hotels](#dim_hotels)
   - [dim_rooms](#dim_rooms)
   - [fact_aggregated_bookings](#fact_aggregated_bookings)
   - [fact_bookings](#fact_bookings)
3. [Usage](#usage)

---

## Datasets

The following CSV files are included:
1. `dim_date.csv`
2. `dim_hotels.csv`
3. `dim_rooms.csv`
4. `fact_aggregated_bookings.csv`
5. `fact_bookings.csv`

---

## Column Descriptions

### 1. dim_date
| Column Name | Description |
|-------------|-------------|
| `date`      | Represents the dates in May, June, and July. |
| `mmm yy`    | Represents the date in the format of `mmm yy` (month name year). |
| `week no`   | Unique week number for that particular date. |
| `day_type`  | Indicates whether the given day is a Weekend or Weekday. |

---

### 2. dim_hotels
| Column Name      | Description |
|------------------|-------------|
| `property_id`    | Unique ID for each hotel. |
| `property_name`  | Name of each hotel. |
| `category`       | Classification of the hotel/property (e.g., Luxury, Business). |
| `city`           | Location of the hotel/property. |

---

### 3. dim_rooms
| Column Name   | Description |
|---------------|-------------|
| `room_id`     | Type of room (e.g., RT1, RT2, RT3, RT4). |
| `room_class`  | Classification of room type (e.g., Standard, Elite, Premium, Presidential). |

---

### 4. fact_aggregated_bookings
| Column Name           | Description |
|-----------------------|-------------|
| `property_id`         | Unique ID for each hotel. |
| `check_in_date`       | All check-in dates of the customers. |
| `room_category`       | Type of room (e.g., RT1, RT2, RT3, RT4). |
| `successful_bookings` | Total successful bookings for a specific room type at a hotel on a given date. |
| `capacity`            | Maximum room count available for a specific room type at a hotel on a given date. |

---

### 5. fact_bookings
| Column Name          | Description |
|----------------------|-------------|
| `booking_id`         | Unique booking ID for each customer. |
| `property_id`        | Unique ID for each hotel. |
| `booking_date`       | Date when the customer booked their room. |
| `check_in_date`      | Date when the customer checked in. |
| `check_out_date`     | Date when the customer checked out. |
| `no_guests`          | Number of guests staying in a room. |
| `room_category`      | Type of room (e.g., RT1, RT2, RT3, RT4). |
| `booking_platform`   | Platform used for booking the room. |
| `ratings_given`      | Ratings provided by the customer for hotel services. |
| `booking_status`     | Status of the booking: `Cancelled`, `Checked Out`, or `No Show`. |
| `revenue_generated`  | Total amount generated by the hotel for a booking. |
| `revenue_realized`   | Final revenue received by the hotel after deductions for cancellations. |

- **Revenue Deduction Rules**:
  - If the booking status is `Cancelled`, 40% of the revenue is refunded to the customer, and 60% is realized by the hotel.
  - For `Checked Out` and `No Show`, 100% of the revenue is realized by the hotel.

---

## Usage

1. **Load the Datasets**: Import the CSV files into your preferred analysis tool (e.g., Python, Excel, Power BI).
2. **Analyze Trends**: Use the data to analyze trends like occupancy rates, revenue performance, and customer preferences.
3. **Visualize Insights**: Create interactive dashboards using Power BI, Tableau, or any other visualization tool.

---