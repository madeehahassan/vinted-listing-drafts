# Listing record

Keep one record per product. JSON, a database or a review page can store it, provided the seller can inspect and edit these fields.

| Field | Meaning |
| --- | --- |
| `item_id` | Stable private reference for this product. |
| `source_photos` | Original filenames, kept unchanged. |
| `listing_photos` | Ordered, selected JPEGs eligible for Vinted upload. |
| `photo_variants` | Accepted and rejected edits with their source photo and reason. |
| `private_reference_photos` | Inventory or number-tag images excluded from uploads. |
| `title`, `description`, `category` | Editable buyer-facing copy and category. |
| `brand`, `size`, `condition`, `colour`, `material`, `quantity` | Attributes with photographed or seller-confirmed evidence. |
| `price_comparisons` | Direct source links, date, currency, condition, match quality and observation type: retail, new sale, resale ask or completed sale. |
| `asking_price`, `currency`, `price_note` | Editable asking price and private rationale. |
| `review_flags` | Exact facts the seller must check. |
| `approval_state` | Needs review, approved for Vinted draft, approved to publish, drafted, published or excluded. |
| `vinted_url`, `transfer_note` | Result and any field mapping or blocker after transfer. |

The seller's latest edit is the current value. A prior proposal is useful for learning preferences but must not overwrite the current record.
