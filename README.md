## 🔐 Payment Integration with Chapa

- Chapa API integrated for secure ETB payments.
- Booking flow now includes:
  1. Initiation of payment using Chapa API.
  2. Verification after payment.
  3. Status tracking (`Pending`, `Completed`, `Failed`).
  4. Confirmation email sent to user (via Celery).

### API Endpoints
- `POST /api/initiate-payment/` — Initiates a payment session.
- `GET /api/verify-payment/?tx_ref=<reference>` — Verifies and updates payment status.
