# updated from the original @ http://cheat.errtheblog.com/s/rspec_shoulda
# just a subset -- models -- is included here. I'll update this, and create cheat sheets for others, as I go along.
# I marked the ones I added with NEW and also added the links to the corresponding code, as I think it's useful.
# Any comments/corrections are welcome!

# =================  Data and Associations =======================
# https://github.com/thoughtbot/shoulda-matchers/tree/master/lib/shoulda/matchers/active_record

it { should_not have_db_column(:admin).of_type(:boolean) }
it { should have_db_column(:salary).
      of_type(:decimal).
      with_options(:precision => 10, :scale => 2) }
it { should have_readonly_attributes(:password) }
it { should belong_to(:parent) }
it { should have_db_index(:id) } # NEW

it { should have_many(:friends) }
it { should have_many(:enemies).through(:friends) }
it { should have_many(:enemies).dependent(:destroy) }

it { should have_one(:god) }

it { should have_and_belong_to_many(:posts) }

it {should accept_nested_attributes_for(:user)} # NEW

# ================== Validation Matchers ============================
# https://github.com/thoughtbot/shoulda-matchers/tree/master/lib/shoulda/matchers/active_model

it { should validate_uniqueness_of(:keyword) }
it { should validate_uniqueness_of(:keyword).with_message(/dup/) }
it { should validate_uniqueness_of(:email).scoped_to(:name) }
it { should validate_uniqueness_of(:email).
              scoped_to(:first_name, :last_name) }
it { should validate_uniqueness_of(:keyword).case_insensitive }

it { should validate_presence_of(:name) }
it { should validate_presence_of(:name).
              with_message(/is not optional/) }

it { should validate_numericality_of(:age) }

it { should validate_format_of(:name).
              with('12345').
              with_message(/is not optional/) }
it { should validate_format_of(:name).
              not_with('12D45').
              with_message(/is not optional/) }

it { should validate_acceptance_of(:eula) }

it { should ensure_length_of(:password).
              is_at_least(6).
              is_at_most(20) }
it { should ensure_length_of(:name).
              is_at_least(3).
              with_short_message(/not long enough/) }
it { should ensure_length_of(:ssn).
              is_equal_to(9).
              with_message(/is invalid/) }

it { should ensure_inclusion_of(:age).in_range(0..100) }
it { should_not allow_mass_assignment_of(:password) }
it { should allow_mass_assignment_of(:first_name) }
it { should validate_format_of(:first_name).with("Carl") }

it { should validate_confirmation_of(:password) } # NEW
