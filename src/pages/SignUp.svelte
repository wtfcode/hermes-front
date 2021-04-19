<script>
    import axios from "axios";
    let countries = [];

    axios
        .get("https://restcountries.eu/rest/v2/all")
        .then((res) => (countries = res.data));
</script>

<div class="bg-dark-blue">
    <div class="container py-4">
        <h1 class="display-1 title">Sign Up</h1>
        <div
            class="is-flex is-justify-content-center is-align-items-center h-100p"
        >
            <div class="column is-three-fifths">
                <div class="card">
                    <div class="card-content">
                        <div class="content">
                            <form>
                                <div class="field">
                                    <label class="label" for="fullname"
                                        >Fullname</label
                                    >
                                    <div class="control has-icons-left">
                                        <input
                                            class="input"
                                            type="text"
                                            placeholder="Your Fullname"
                                            id="fullname"
                                        />
                                        <span class="icon is-small is-left">
                                            <i class="fas fa-user" />
                                        </span>
                                    </div>
                                </div>
                                <div class="field">
                                    <label class="label" for="email"
                                        >Email Address</label
                                    >
                                    <div class="control has-icons-left">
                                        <input
                                            class="input"
                                            type="email"
                                            placeholder="Your Email Address"
                                            id="email"
                                        />
                                        <span class="icon is-small is-left">
                                            <i class="fas fa-envelope" />
                                        </span>
                                    </div>
                                </div>
                                <div class="columns">
                                    <div class="column">
                                        <div class="field">
                                            <label
                                                class="label"
                                                for="select-country"
                                                >Country</label
                                            >
                                            <div class="control">
                                                <div
                                                    class="select is-fullwidth"
                                                >
                                                    <select id="select-country">
                                                        <option>
                                                            Select Your Country
                                                        </option>
                                                        {#each countries as country}
                                                            <option
                                                                value={country.alpha3Code}
                                                            >
                                                                {country.name}
                                                            </option>
                                                        {/each}
                                                    </select>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="column">
                                        <div class="field">
                                            <label
                                                class="label"
                                                for="tel-number"
                                                >Telephone Number</label
                                            >
                                            <div class="control has-icons-left">
                                                <input
                                                    class="input"
                                                    type="text"
                                                    placeholder="Your Telephone Number"
                                                    id="tel-number"
                                                />
                                                <span
                                                    class="icon is-small is-left"
                                                >
                                                    <i class="fas fa-phone" />
                                                </span>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="field">
                                    <label class="label" for="company"
                                        >Company</label
                                    >
                                    <div class="control has-icons-left">
                                        <input
                                            class="input"
                                            type="text"
                                            placeholder="Your Company"
                                            id="company"
                                        />
                                        <span class="icon is-small is-left">
                                            <i class="fas fa-building" />
                                        </span>
                                    </div>
                                </div>
                                <div class="columns">
                                    <div class="column">
                                        <div class="field">
                                            <label
                                                class="label"
                                                for="departament"
                                                >Departament</label
                                            >
                                            <div class="control">
                                                <div
                                                    class="select is-fullwidth"
                                                >
                                                    <select id="departament">
                                                        <option
                                                            >Administration</option
                                                        >
                                                        <option
                                                            >Accounting</option
                                                        >
                                                    </select>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="column">
                                        <div class="field">
                                            <label class="label" for="id-number"
                                                >ID Number</label
                                            >
                                            <div class="control has-icons-left">
                                                <input
                                                    class="input"
                                                    type="text"
                                                    placeholder="Your ID Number"
                                                    id="id-number"
                                                />
                                                <span
                                                    class="icon is-small is-left"
                                                >
                                                    <i class="fas fa-hashtag" />
                                                </span>
                                            </div>
                                        </div>
                                    </div>
                                </div>

                                <div class="field mb-5">
                                    <label class="label" for="password"
                                        >Password</label
                                    >
                                    <div class="control has-icons-left">
                                        <input
                                            class="input"
                                            type="password"
                                            placeholder="Create a Password"
                                            id="password"
                                        />
                                        <span class="icon is-small is-left">
                                            <i class="fas fa-lock" />
                                        </span>
                                    </div>
                                </div>

                                <div class="field">
                                    <div class="control">
                                        <button
                                            class="button is-fullwidth btn-yellow"
                                        >
                                            Sign Up
                                        </button>
                                    </div>
                                </div>
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
